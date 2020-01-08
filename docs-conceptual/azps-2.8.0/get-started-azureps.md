---
title: Ismerkedés az Azure PowerShell-lel
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c515fcbbe4dcb0b6578a56da137a77e3f843a2e6
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/07/2020
ms.locfileid: "75720446"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="8bff4-102">Ismerkedés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="8bff4-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="8bff4-103">Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására készült.</span><span class="sxs-lookup"><span data-stu-id="8bff4-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="8bff4-104">Az Azure PowerShellt olyan automatizált eszközök létrehozására használhatja, amelyek az Azure Resource Manager modellt használják.</span><span class="sxs-lookup"><span data-stu-id="8bff4-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="8bff4-105">Próbálja ki a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítse a helyi számítógépen.</span><span class="sxs-lookup"><span data-stu-id="8bff4-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="8bff4-106">A cikk segítséget nyújt az Azure PowerShell használatának megkezdésében, és ismerteti az alapvető fogalmakat.</span><span class="sxs-lookup"><span data-stu-id="8bff4-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="8bff4-107">Telepítés vagy futtatás az Azure Cloud Shellben</span><span class="sxs-lookup"><span data-stu-id="8bff4-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="8bff4-108">Az Azure PowerShell használatát úgy kezdheti meg a legegyszerűbben, ha kipróbálja egy Azure Cloud Shell-környezetben.</span><span class="sxs-lookup"><span data-stu-id="8bff4-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="8bff4-109">A Cloud Shell gyors üzembe helyezéséhez tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="8bff4-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="8bff4-110">A Cloud Shell Linux-tárolón futtatja a PowerShell 6-ot, ezért a Windows-specifikus szolgáltatások nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="8bff4-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="8bff4-111">Ha készen áll az Azure PowerShell helyi számítógépen történő telepítésére, kövesse az [Azure PowerShell modul telepítése](install-az-ps.md) című részben leírt utasításokat.</span><span class="sxs-lookup"><span data-stu-id="8bff4-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="8bff4-112">Bejelentkezés az Azure-ba</span><span class="sxs-lookup"><span data-stu-id="8bff4-112">Sign in to Azure</span></span>

<span data-ttu-id="8bff4-113">Jelentkezzen be interaktívan a `Connect-AzAccount` parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8bff4-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="8bff4-114">Ha a Cloud Shellt használja, hagyja ki ezt a lépést: Az Azure Cloud Shell-munkamenet már hitelesítve lett a környezet, az előfizetés és a Cloud Shell-munkamenetet elindító bérlő esetében.</span><span class="sxs-lookup"><span data-stu-id="8bff4-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="8bff4-115">Ha az Egyesült Államokon kívüli régióban van, a bejelentkezéshez használja az `-Environment` paramétert.</span><span class="sxs-lookup"><span data-stu-id="8bff4-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="8bff4-116">A [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) parancsmaggal kérje le a régiójához tartozó környezet nevét.</span><span class="sxs-lookup"><span data-stu-id="8bff4-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="8bff4-117">Például az Azure China 21Vianetbe történő bejelentkezéshez:</span><span class="sxs-lookup"><span data-stu-id="8bff4-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="8bff4-118">PowerShell 5.1-környezetekben egy bejelentkezési párbeszédpanelen kell megadnia az Azure-fiókjához tartozó felhasználónevet és jelszót.</span><span class="sxs-lookup"><span data-stu-id="8bff4-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="8bff4-119">A többi PowerShell-verzió esetében kap egy jogkivonatot, amelyet a [https://microsoft.com/devicelogin ] címen használhat.</span><span class="sxs-lookup"><span data-stu-id="8bff4-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="8bff4-120">Nyissa meg ezt az oldalt a böngészőjében, és írja be a jogkivonatot, majd jelentkezzen be az Azure-fiókjának hitelesítő adataival, és engedélyezze az Azure PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="8bff4-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="8bff4-121">A bejelentkezést követően az aktív Azure-előfizetésre vonatkozó információk jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="8bff4-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="8bff4-122">Ha a fiókjához több Azure-előfizetés is tartozik, és egy másikat szeretne kiválasztani, kérje le az elérhető előfizetéseket a [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) segítségével, majd futtassa a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot az előfizetés azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="8bff4-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="8bff4-123">További információk az Azure-előfizetések felügyeletéről az Azure PowerShellben: [Több Azure-előfizetés használata](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8bff4-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="8bff4-124">Miután bejelentkezett, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="8bff4-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="8bff4-125">A bejelentkezési folyamattal és a hitelesítési módszerekkel kapcsolatos további információért tekintse meg az [Azure PowerShell-lel való bejelentkezést](authenticate-azureps.md) bemutató cikket.</span><span class="sxs-lookup"><span data-stu-id="8bff4-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="8bff4-126">Parancsok keresése</span><span class="sxs-lookup"><span data-stu-id="8bff4-126">Find commands</span></span>

<span data-ttu-id="8bff4-127">Az Azure PowerShell-parancsmagok a PowerShell esetében standard elnevezési konvenciót követnek: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="8bff4-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="8bff4-128">Az ige leírja a műveletet (például `New`, `Get`, `Set`, `Remove`), a főnév pedig az erőforrástípust (például `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="8bff4-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="8bff4-129">Az Azure PowerShellben a főnevek mindig az `Az` előtaggal kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="8bff4-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="8bff4-130">A standard igék teljes listájáért tekintse meg a következőt: [PowerShell-parancsokhoz jóváhagyott igék](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="8bff4-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="8bff4-131">A főnevek, igék és az elérhető Azure PowerShell-modulok ismerete segít megtalálni a parancsokat a [Get-Command](/powershell/module/microsoft.powershell.core/get-command) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="8bff4-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="8bff4-132">Például az összes, `Get` igét tartalmazó, virtuális géphez kapcsolódó parancs megkereséséhez:</span><span class="sxs-lookup"><span data-stu-id="8bff4-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="8bff4-133">A gyakori parancsok megtalálásának megkönnyítéséhez ez a táblázat felsorolja az erőforrástípusokat, a megfelelő Azure PowerShell-modulokat és a `Get-Command` paranccsal használható főnévi előtagokat:</span><span class="sxs-lookup"><span data-stu-id="8bff4-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="8bff4-134">Erőforrás típusa</span><span class="sxs-lookup"><span data-stu-id="8bff4-134">Resource type</span></span> | <span data-ttu-id="8bff4-135">Azure PowerShell-modul</span><span class="sxs-lookup"><span data-stu-id="8bff4-135">Azure PowerShell module</span></span> | <span data-ttu-id="8bff4-136">Főnévi előtag</span><span class="sxs-lookup"><span data-stu-id="8bff4-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="8bff4-137">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="8bff4-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="8bff4-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8bff4-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="8bff4-139">Virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="8bff4-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="8bff4-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8bff4-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="8bff4-141">Tárfiókok</span><span class="sxs-lookup"><span data-stu-id="8bff4-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="8bff4-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8bff4-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="8bff4-143">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8bff4-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="8bff4-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8bff4-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="8bff4-145">Webalkalmazások</span><span class="sxs-lookup"><span data-stu-id="8bff4-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="8bff4-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8bff4-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="8bff4-147">SQL-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="8bff4-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="8bff4-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8bff4-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="8bff4-149">Az Azure PowerShellben található modulok teljes listáját a GitHubon, az [Azure PowerShell-modulok listájában](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) találja.</span><span class="sxs-lookup"><span data-stu-id="8bff4-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="8bff4-150">Az Azure PowerShell alapjainak megismerése rövid útmutatók és oktatóanyagok segítségével</span><span class="sxs-lookup"><span data-stu-id="8bff4-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="8bff4-151">Az Azure PowerShell használatának megkezdéséhez tekintsen meg egy részletes oktatóanyagot a virtuális gépek beállításáról, valamint azok lekérdezéséről.</span><span class="sxs-lookup"><span data-stu-id="8bff4-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8bff4-152">Virtuális gépek létrehozása az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="8bff4-152">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="8bff4-153">Egyéb népszerű Azure-szolgáltatásokhoz is elérhetők rövid Azure PowerShell-útmutatók:</span><span class="sxs-lookup"><span data-stu-id="8bff4-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="8bff4-154">Tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="8bff4-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="8bff4-155">Objektumok továbbítása Azure Blob-tárolókra és -tárolókról</span><span class="sxs-lookup"><span data-stu-id="8bff4-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="8bff4-156">Titkos kulcsok létrehozása és lekérése az Azure Key Vaultból</span><span class="sxs-lookup"><span data-stu-id="8bff4-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="8bff4-157">Azure SQL-adatbázis és tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="8bff4-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="8bff4-158">Tároló futtatása az Azure Container Instancesben</span><span class="sxs-lookup"><span data-stu-id="8bff4-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="8bff4-159">Virtuálisgép-méretezési csoport (VMSS) létrehozása</span><span class="sxs-lookup"><span data-stu-id="8bff4-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="8bff4-160">Standard terheléselosztó létrehozása</span><span class="sxs-lookup"><span data-stu-id="8bff4-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="8bff4-161">További lépések</span><span class="sxs-lookup"><span data-stu-id="8bff4-161">Next steps</span></span>

* [<span data-ttu-id="8bff4-162">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="8bff4-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="8bff4-163">Azure-előfizetések kezelése az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="8bff4-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="8bff4-164">Szolgáltatásnevek létrehozása az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="8bff4-164">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="8bff4-165">Segítség kérése a közösségtől:</span><span class="sxs-lookup"><span data-stu-id="8bff4-165">Get help from the community:</span></span>
  * [<span data-ttu-id="8bff4-166">Azure-fórum az MSDN-en</span><span class="sxs-lookup"><span data-stu-id="8bff4-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="8bff4-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="8bff4-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
