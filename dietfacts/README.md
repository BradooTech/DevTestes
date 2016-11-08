# OdooTest
Testes realizados no Odoo
<<<<<<< HEAD
Tentativa 1

up vote
63
down vote
In this particular use case, you don't really want to abort the merge, just resolve the conflict in a particular way.

There is no particular need to reset and perform a merge with a different strategy, either. The conflicts have been correctly highlighted by git and the requirement to accept the other sid
=======

	

>>>>>>> 84405b2fc452d786919bec9ffeda6ff384fad25d




<<<<<<< HEAD










if the value can be evaluated(like res_id is available), we write value tag as follows:

    - !function {model: account.invoice, name: pay_and_reconcile}: - eval: "obj(ref('test_order_1')).amount_total" model: sale.orde77777777777777777777777777777777777777777777777777777777777777r
adsadadasdasdasdasdsadasdas
    This will fetch the 'amount_total' value of a 'sale.order' record with res_id 'test_ordehed on some model based on a criteria, we write value tag as follows:

    - !function {model: account.invoice, name: pay_and_reconcile}: - model: account.account search: "[('type', '=', 'cash')]" This will fetch all those account.account records whose type is equal to 'cas-

    !python {model: ac
        self.action_move_cre draft state:

-

    !assert {model: account.invoice , id: invoice1, string: "the invoice is now in Draft state"}:

        - state == "draft"8555555555555555555555555556666666

To test that all account are in a tree data structure, we write the below python code:

-

    !python {model: account.account}:

        ids = self.search(cr, uid, [])

        accounts_list = self.read(cr, uid, ids['parent_id','parent_left','parent_right'])

        accounts = dict((x['id'], x) for x in accounts_list)

        log("Testing parent structure for %d accounts", len(accounts_list))

        for a in accounts_list:

            if a['parent_id']:

                assert a['parent_left']>accounts[a['parent_id'][0]]['parent_left']

                assert a['parent_right']<accounts[a['parent_id'][0]]['parent_right']

            assert a['parent_left']<a['parent_right']

        for a2 in accounts_list:

            assert not ((a2['parent_right']>a['parent_left'])and

                (a2['parent_left']<a['parent_left'])and

,554544545                (a2['parent_right']<a['parent_right']))

                if a2['parent_id']==a['id']:

               

        Save the file with '.yml' extention

        Add the yaml file under 'demo_xml' in terp file

        Run the server with '--log-level=test' opt6566666666666

111111111111111111111111111111111111111111111111111111111
=======
You can directly do:

git checkout <original-remote-branch-name>
This automatically creates a local branch which tracks the remote branch with the same name. Do this always after cloning, if you want to work on a particular branch other than master.

Note: When you clone the remote name is by default 'origin' which is different from the remote name used in other machines where you are developing. So, you can initially name your remote before cloning or push to origin ever after.
>>>>>>> 84405b2fc452d786919bec9ffeda6ff384fad25d
