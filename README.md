# bitrix_highloadblock_class

Welcome to the bitrix_highloadblock_class wiki!

Using:
require_once('hlb.class');
$hl_block = new Hlb(_highloadblock_table_name_);
$hl_block->Select(_field_,_value_,_logic_operation_)
где:
_field_ - поле фильтра
_value_ - аргумент логической операции
_logic_operation_ - логическая операция:
* = равно (работает и с массивами)
* % подстрока
* > больше
* < меньше
* @ IN (EXPR), в качестве значения передается объект DB\SqlExpression
* !@ NOT IN (EXPR), в качестве значения передается объект DB\SqlExpression
* != не равно
* !% не подстрока
* >< между, в качестве значения передается массив array(MIN, MAX)
* >= больше или равно
* <= меньше или равно
* =% LIKE
* %= LIKE
* == булевое выражение для ExpressionField (например, для EXISTS() или NOT EXISTS())
* !>< не между, в качестве значения передается массив array(MIN, MAX)
* !=% NOT LIKE
* !%= NOT LIKE
* '==ID' => null строгое сравнение с NULL по ID
* '!==NAME' => null строгое сравнение с NULL по NAME
