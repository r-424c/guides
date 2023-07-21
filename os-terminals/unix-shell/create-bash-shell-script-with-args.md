


> real example:
```sh
today=$(date +"%Y-%m-%d")
mysqldump_path="mysql-src/bin/mysqldump.exe"

cnf_prod_server=' '
prod_server_target=' '
file_result=' '
db_name=' '


for i in "$@"; do
  case $i in
    --cnf-file=*)
      cnf_prod_server="${i#*=}"
      shift # past argument=value
      ;;
    --output-file=*)
      file_result="${i#*=}"
      shift # past argument=value
      ;;
    --database=*)
      db_name="${i#*=}"
      shift # past argument=value
      ;;
    --server=*)
      prod_server_target="${i#*=}"
      prod_server_target=`echo $prod_server_target | tr 'a-z' 'A-Z'` # required
      shift # past argument=value
      ;;
    -*|--*)
      echo "Unknown option $i"
      exit 1
      ;;
    *)
      ;;
  esac
done

parameters=("$cnf_prod_server" "$file_result" "$db_name" "$prod_server_target")

for i in "${parameters[@]}"
do
   if [ -z "${i// }" ]
   then
      echo "Missing parameter, check required --cnf-file=, --output-file=, --database=, --server="
      exit 1
   fi  
done

output_filename=`basename "$file_result" .sql`
file="updates/$prod_server_target/$output_filename-${today}.sql"

```


refereces:
- https://stackoverflow.com/a/14203146/13493399
- https://stackoverflow.com/a/46237844/13493399