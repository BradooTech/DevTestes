# OdooTest
Testes realizados no Odoo
Tentativa 1

up vote
58
down vote
In this particular use case, you don't really want to abort the merge, just resolve the conflict in a particular way.

There is no particular need to reset and perform a merge with a different strategy, either. The conflicts have been correctly highlighted by git and the requirement to accept the other sid
=======

	

>>>>>>> 84405b2fc452d786919bec9ffeda6ff384fad25d




<<<<<<< HEAD








if the value can be evaluated(like res_id is available), we write value tag as follows:

    - !function {model: account.invoice, name: pay_and_reconcile}: - eval: "obj(ref('test_order_1')).amount_total" model: sale.order

    This will fetch the 'amount_total' value of a 'sale.order' record with res_id 'test_order_1'

If the value is to be searched on some model based on a criteria, we write value tag as follows:

    - !function {model: account.invoice, name: pay_and_reconcile}: - model: account.account search: "[('type', '=', 'cash')]" This will fetch all those account.account records whose type is equal to 'cas

[kkkkkllllllllllllllll]
[kkllllllllll]
-
=======
if the value can be evaluated(like res_id is available), we write value tag as follows:
>>>>>>> dev_test_Marcio

    !python {model: account.invoice}: |

        self.action_move_create(cr, uid, [ref("invoice1")])

The invoice must be in draft state:

-

    !assert {model: account.invoice , id: invoice1, string: "the invoice is now in Draft state"}:

        - state == "draft"

To test that all account are in a tree data structure, we write the below python code:

-
[´´´´´´´´]
    python {model: account.account}:

        ids = self.search(cr, uid, [])

        accounts_list = self.read(cr, uid, ids['parent_id','parent_left','parent_right'])

        accounts = dict((x['id'], x) for x in accounts_list)

    

        for a in accounts_list:

            if a['parent_id']:

                assert a['parent_left']>accounts[a['parent_id'][0]]['parent_left']

                assert a['parent_right']<accounts[a['parent_id'][0]]['parent_right']

            assert a['parent_left']<a['parent_right']

        for a2 in accounts_list:

            assert not ((a2['parent_right']>a['parent_left'])and

                (a2['parent_left']<a['parent_left'])and

                (a2['parent_right']<a['parent_right']))

                if a2['parent_id']==a['id']:

                    assert(a2['parent_left']>a['parent_left'])and(a2['parent_right']<a['parent_right'])

Running tests

        Save the file with '.yml' extention

        Add the yaml file under 'demo_xml' in terp file

        Run the server with '--log-level=test' option

111111111111111111111111111111111111111111111111111111111
=======
You can directly do:

git checkout <original-remote-branch-name>
This automatically creates a local branch which tracks the remote branch with the same name. Do this always after cloning, if you want to work on a particular branch other than master.

<<<<<<< HEAD
11111111111111111222222222222222222222222222223333333333333333333333333333333

44444

55

1


