---
title: Ismerkedés az Azure PowerShell-lel
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c60036ba8be6282007aa34a0bb9c0d9e33197072
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657671"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="0b679-102">Ismerkedés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0b679-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="0b679-103">Az Azure PowerShell az Azure-erőforrások parancssori kezelésére és adminisztrálására készült.</span><span class="sxs-lookup"><span data-stu-id="0b679-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="0b679-104">Az Azure PowerShellt olyan automatizált eszközök létrehozására használhatja, amelyek az Azure Resource Manager modellt használják.</span><span class="sxs-lookup"><span data-stu-id="0b679-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="0b679-105">Próbálja ki a böngészőjében az [Azure Cloud Shell-lel](/azure/cloud-shell/overview), vagy telepítse a helyi számítógépen.</span><span class="sxs-lookup"><span data-stu-id="0b679-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="0b679-106">A cikk segítséget nyújt az Azure PowerShell használatának megkezdésében, és ismerteti az alapvető fogalmakat.</span><span class="sxs-lookup"><span data-stu-id="0b679-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="0b679-107">Telepítés vagy futtatás az Azure Cloud Shellben</span><span class="sxs-lookup"><span data-stu-id="0b679-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="0b679-108">Az Azure PowerShell használatát úgy kezdheti meg a legegyszerűbben, ha kipróbálja egy Azure Cloud Shell-környezetben.</span><span class="sxs-lookup"><span data-stu-id="0b679-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="0b679-109">A Cloud Shell gyors üzembe helyezéséhez tekintse meg a [PowerShell Azure Cloud Shellben való használatát bemutató rövid útmutatót](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="0b679-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="0b679-110">A Cloud Shell Linux-tárolón futtatja a PowerShell 6-ot, ezért a Windows-specifikus szolgáltatások nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="0b679-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="0b679-111">Ha készen áll az Azure PowerShell helyi számítógépen történő telepítésére, kövesse az [Azure PowerShell modul telepítése](install-az-ps.md) című részben leírt utasításokat.</span><span class="sxs-lookup"><span data-stu-id="0b679-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="0b679-112">Bejelentkezés az Azure-ba</span><span class="sxs-lookup"><span data-stu-id="0b679-112">Sign in to Azure</span></span>

<span data-ttu-id="0b679-113">Jelentkezzen be interaktívan a `Connect-AzAccount` parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0b679-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="0b679-114">Ha a Cloud Shellt használja, hagyja ki ezt a lépést: Az Azure Cloud Shell-munkamenet már hitelesítve lett a környezet, az előfizetés és a Cloud Shell-munkamenetet elindító bérlő esetében.</span><span class="sxs-lookup"><span data-stu-id="0b679-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="0b679-115">Ha az Egyesült Államokon kívüli régióban van, a bejelentkezéshez használja az `-Environment` paramétert.</span><span class="sxs-lookup"><span data-stu-id="0b679-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="0b679-116">A [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) parancsmaggal kérje le a régiójához tartozó környezet nevét.</span><span class="sxs-lookup"><span data-stu-id="0b679-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="0b679-117">Például az Azure China 21Vianetbe történő bejelentkezéshez:</span><span class="sxs-lookup"><span data-stu-id="0b679-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="0b679-118">Kap egy jogkivonatot, amelyet a https://microsoft.com/devicelogin címen használhat.</span><span class="sxs-lookup"><span data-stu-id="0b679-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="0b679-119">Nyissa meg ezt az oldalt a böngészőjében, és írja be a jogkivonatot, majd jelentkezzen be az Azure-fiókjának hitelesítő adataival, és engedélyezze az Azure PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="0b679-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="0b679-120">A bejelentkezést követően az aktív Azure-előfizetésre vonatkozó információk jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="0b679-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="0b679-121">Ha a fiókjához több Azure-előfizetés is tartozik, és egy másikat szeretne kiválasztani, kérje le az elérhető előfizetéseket a [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) segítségével, majd futtassa a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot az előfizetés azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="0b679-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="0b679-122">További információk az Azure-előfizetések felügyeletéről az Azure PowerShellben: [Több Azure-előfizetés használata](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0b679-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="0b679-123">Miután bejelentkezett, az Azure PowerShell parancsmagjaival elérheti és kezelheti az előfizetésben lévő erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="0b679-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="0b679-124">A bejelentkezési folyamattal és a hitelesítési módszerekkel kapcsolatos további információért tekintse meg az [Azure PowerShell-lel való bejelentkezést](authenticate-azureps.md) bemutató cikket.</span><span class="sxs-lookup"><span data-stu-id="0b679-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="0b679-125">Parancsok keresése</span><span class="sxs-lookup"><span data-stu-id="0b679-125">Find commands</span></span>

<span data-ttu-id="0b679-126">Az Azure PowerShell-parancsmagok a PowerShell esetében standard elnevezési konvenciót követnek: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="0b679-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="0b679-127">Az ige leírja a műveletet (például `New`, `Get`, `Set`, `Remove`), a főnév pedig az erőforrástípust (például `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="0b679-127">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="0b679-128">Az Azure PowerShellben a főnevek mindig az `Az` előtaggal kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="0b679-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="0b679-129">A standard igék teljes listájáért tekintse meg a következőt: [PowerShell-parancsokhoz jóváhagyott igék](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="0b679-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="0b679-130">A főnevek, igék és az elérhető Azure PowerShell-modulok ismerete segít megtalálni a parancsokat a [Get-Command](/powershell/module/microsoft.powershell.core/get-command) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="0b679-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="0b679-131">Például az összes, `Get` igét tartalmazó, virtuális géphez kapcsolódó parancs megkereséséhez:</span><span class="sxs-lookup"><span data-stu-id="0b679-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="0b679-132">A gyakori parancsok megtalálásának megkönnyítéséhez ez a táblázat felsorolja az erőforrástípusokat, a megfelelő Azure PowerShell-modulokat és a `Get-Command` paranccsal használható főnévi előtagokat:</span><span class="sxs-lookup"><span data-stu-id="0b679-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="0b679-133">Erőforrás típusa</span><span class="sxs-lookup"><span data-stu-id="0b679-133">Resource type</span></span> | <span data-ttu-id="0b679-134">Azure PowerShell-modul</span><span class="sxs-lookup"><span data-stu-id="0b679-134">Azure PowerShell module</span></span> | <span data-ttu-id="0b679-135">Főnévi előtag</span><span class="sxs-lookup"><span data-stu-id="0b679-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="0b679-136">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="0b679-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="0b679-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b679-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="0b679-138">Virtuális gépek</span><span class="sxs-lookup"><span data-stu-id="0b679-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="0b679-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b679-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="0b679-140">Tárfiókok</span><span class="sxs-lookup"><span data-stu-id="0b679-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="0b679-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b679-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="0b679-142">Key Vault</span><span class="sxs-lookup"><span data-stu-id="0b679-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="0b679-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b679-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="0b679-144">Webalkalmazások</span><span class="sxs-lookup"><span data-stu-id="0b679-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="0b679-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b679-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="0b679-146">SQL-adatbázisok</span><span class="sxs-lookup"><span data-stu-id="0b679-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="0b679-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b679-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="0b679-148">Az Azure PowerShellben található modulok teljes listáját a GitHubon, az [Azure PowerShell-modulok listájában](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) találja.</span><span class="sxs-lookup"><span data-stu-id="0b679-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="0b679-149">Az Azure PowerShell alapjainak megismerése rövid útmutatók és oktatóanyagok segítségével</span><span class="sxs-lookup"><span data-stu-id="0b679-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="0b679-150">Az Azure PowerShell használatának megkezdéséhez tekintsen meg egy részletes oktatóanyagot a virtuális gépek beállításáról, valamint azok lekérdezéséről.</span><span class="sxs-lookup"><span data-stu-id="0b679-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="0b679-151">Virtuális gépek létrehozása az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0b679-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="0b679-152">Egyéb népszerű Azure-szolgáltatásokhoz is elérhetők rövid Azure PowerShell-útmutatók:</span><span class="sxs-lookup"><span data-stu-id="0b679-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="0b679-153">Tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b679-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="0b679-154">Objektumok továbbítása Azure Blob-tárolókra és -tárolókról</span><span class="sxs-lookup"><span data-stu-id="0b679-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="0b679-155">Titkos kulcsok létrehozása és lekérése az Azure Key Vaultból</span><span class="sxs-lookup"><span data-stu-id="0b679-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="0b679-156">Azure SQL-adatbázis és tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b679-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="0b679-157">Tároló futtatása az Azure Container Instancesben</span><span class="sxs-lookup"><span data-stu-id="0b679-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="0b679-158">Virtuálisgép-méretezési csoport (VMSS) létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b679-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="0b679-159">Standard terheléselosztó létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b679-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="0b679-160">További lépések</span><span class="sxs-lookup"><span data-stu-id="0b679-160">Next steps</span></span>

* [<span data-ttu-id="0b679-161">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0b679-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="0b679-162">Azure-előfizetések kezelése az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0b679-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="0b679-163">Szolgáltatásnevek létrehozása az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="0b679-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="0b679-164">Segítség kérése a közösségtől:</span><span class="sxs-lookup"><span data-stu-id="0b679-164">Get help from the community:</span></span>
  * [<span data-ttu-id="0b679-165">Azure-fórum az MSDN-en</span><span class="sxs-lookup"><span data-stu-id="0b679-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="0b679-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="0b679-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
