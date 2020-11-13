---
title: Ismerkedés az Azure PowerShell-lel
description: Ismerkedés az Azure PowerShell-lel
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 68b2b50afdd2dc79bdbd8f8b203a7cd3664c4973
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409215"
---
# <a name="get-started-with-azure-powershell"></a>Ismerkedés az Azure PowerShell-lel

Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására készült.
Az Azure PowerShellt olyan automatizált eszközök létrehozására használhatja, amelyek az Azure Resource Manager modellt használják. Próbálja ki a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítse a helyi számítógépen.

A cikk segítséget nyújt az Azure PowerShell használatának megkezdésében, és ismerteti az alapvető fogalmakat.

## <a name="install-or-run-in-azure-cloud-shell"></a>Telepítés vagy futtatás az Azure Cloud Shellben

Az Azure PowerShell használatát úgy kezdheti meg a legegyszerűbben, ha kipróbálja egy Azure Cloud Shell-környezetben. A Cloud Shell gyors üzembe helyezéséhez tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell). A Cloud Shell Linux-tárolón futtatja a PowerShellt, ezért a Windows-specifikus funkciók nem érhetők el.

Ha készen áll az Azure PowerShell helyi számítógépen történő telepítésére, kövesse az [Azure PowerShell modul telepítése](install-az-ps.md) című részben leírt utasításokat.

## <a name="sign-in-to-azure"></a>Bejelentkezés az Azure-ba

Jelentkezzen be interaktívan a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmaggal. Ha a Cloud Shellt használja, hagyja ki ezt a lépést. Az Azure Cloud Shell-munkamenet már hitelesítve lett a környezet, az előfizetés és a Cloud Shell-munkamenetet elindító bérlő esetében.

```azurepowershell-interactive
Connect-AzAccount
```

Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak. Regionális felhőszolgáltatásban található fiókok esetében használja az **Environment** paramétert a bejelentkezéshez. A [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) parancsmaggal kérje le a régiójához tartozó környezet nevét.
Például az Azure China 21Vianetbe történő bejelentkezéshez:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Windows PowerShell 5.1-környezetekben egy bejelentkezési párbeszédpanelen kell megadnia az Azure-fiókjához tartozó felhasználónevet és jelszót. A PowerShell többi verziója esetében kap egy jogkivonatot, amelyet a [microsoft.com/devicelogin](https://microsoft.com/devicelogin) címen használhat. Nyissa meg ezt az oldalt a böngészőjében, és írja be a jogkivonatot, majd jelentkezzen be az Azure-fiókjának hitelesítő adataival, és engedélyezze az Azure PowerShellt.

A bejelentkezést követően az aktív Azure-előfizetésre vonatkozó információk jelennek meg. Ha a fiókjához több Azure-előfizetés is tartozik, és egy másikat szeretne kiválasztani, kérje le az elérhető előfizetéseket a [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) segítségével, majd futtassa a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot az előfizetés azonosítójával. További információk az Azure-előfizetések felügyeletéről az Azure PowerShellben: [Több Azure-előfizetés használata](manage-subscriptions-azureps.md).

Miután bejelentkezett, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat. A bejelentkezési folyamattal és a hitelesítési módszerekkel kapcsolatos további információért tekintse meg az [Azure PowerShell-lel való bejelentkezést](authenticate-azureps.md) bemutató cikket.

## <a name="find-commands"></a>Parancsok keresése

Az Azure PowerShell-parancsmagok a PowerShell esetében standard elnevezési konvenciót követnek: `Verb-Noun`. Az ige leírja a műveletet (például `New`, `Get`, `Set`, `Remove`), a főnév pedig az erőforrástípust (például `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). Az Azure PowerShellben a főnevek mindig az `Az` előtaggal kezdődnek. A standard igék teljes listájáért tekintse meg a következőt: [PowerShell-parancsokhoz jóváhagyott igék](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

A főnevek, igék és az elérhető Azure PowerShell-modulok ismerete segít megtalálni a parancsokat a [Get-Command](/powershell/module/microsoft.powershell.core/get-command) parancsmaggal. Például az összes, `Get` igét tartalmazó, virtuális géphez kapcsolódó parancs megkereséséhez:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

A gyakori parancsok megtalálásának megkönnyítéséhez ez a táblázat felsorolja az erőforrástípusokat, a megfelelő Azure PowerShell-modulokat és a `Get-Command` paranccsal használható főnévi előtagokat:

|                              Erőforrás típusa                              |                   Azure PowerShell-modul                    |    Főnévi előtag     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [Erőforráscsoport](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [Virtuális gépek](/azure/virtual-machines)                             | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [Tárfiókok](/azure/storage/common/storage-introduction)          | [Az.Storage](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [Key Vault](/azure/key-vault/key-vault-whatis)                          | [Az.KeyVault](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [Webalkalmazások](/azure/app-service)                                  | [Az.Websites](/powershell/module/az.websites)                | `AzWebApp`         |
| [SQL-adatbázisok](/azure/sql-database)                                    | [Az.Sql](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

Az Azure PowerShellben található modulok teljes listáját a GitHubon, az [Azure PowerShell-modulok listájában](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) találja.

## <a name="telemetry"></a>Telemetria

Az Azure PowerShell alapértelmezés szerint gyűjti a telemetriai adatokat. A Microsoft összesíti a gyűjtött adatokat a használati minták felismerése, a gyakori problémák észlelése és az Azure PowerShell nyújtotta felhasználói élmény javítása érdekében. A Microsoft Azure PowerShell nem gyűjt magánjellegű vagy személyes adatokat. Az adatgyűjtés letiltásához külön el kell utasítania az adatgyűjtést a [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection) futtatásával.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Az Azure PowerShell alapjainak megismerése rövid útmutatók és oktatóanyagok segítségével

Az Azure PowerShell használatának megkezdéséhez tekintsen meg egy részletes oktatóanyagot a virtuális gépek beállításáról, valamint azok lekérdezéséről.

> [!div class="nextstepaction"]
> [Virtuális gépek létrehozása az Azure PowerShell-lel](azureps-vm-tutorial.yml)

Egyéb népszerű Azure-szolgáltatásokhoz is elérhetők rövid Azure PowerShell-útmutatók:

* [Tárfiók létrehozása](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Objektumok továbbítása Azure Blob-tárolókra és -tárolókról](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Titkos kulcsok létrehozása és lekérése az Azure Key Vaultból](/azure/key-vault/quick-create-powershell)
* [Azure SQL-adatbázis és tűzfal létrehozása](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Tároló futtatása az Azure Container Instancesben](/azure/container-instances/container-instances-quickstart-powershell)
* [Virtuálisgép-méretezési csoport létrehozása](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Standard terheléselosztó létrehozása](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>További lépések

* [Bejelentkezés az Azure PowerShell-lel](authenticate-azureps.md)
* [Azure-előfizetések kezelése az Azure PowerShell-lel](manage-subscriptions-azureps.md)
* [Szolgáltatásnevek létrehozása az Azure PowerShell-lel](create-azure-service-principal-azureps.md)
* Segítség kérése a közösségtől:
  * [Azure-fórum az MSDN-en](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
