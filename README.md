csqoop
======

customized sqoop to migrate data from MySQL to HBase



Problem:
1 the column name should be shorter in HBase, so during the migration, the name should be able to be changed with the 'as'
  This can be solved by wrap the select clause again. For example
  select des from (
     select description as des from info
  ) as inf where $CONDITIONS

