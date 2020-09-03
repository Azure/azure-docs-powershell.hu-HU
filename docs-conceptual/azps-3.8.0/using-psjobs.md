---
title: Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban
description: Arra vonatkozó tájékoztatás, hogyan futtathat Azure PowerShell-parancsmagokat párhuzamosan vagy háttérfeladatként az -AsJob és a Start-Job segítségével.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243072"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="82fa8-103">Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban</span><span class="sxs-lookup"><span data-stu-id="82fa8-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="82fa8-104">Az Azure PowerShell működése az Azure-felhőkhöz való csatlakozástól és az onnan kapott válaszoktól függ, ezért a parancsmagok többsége blokkolja a PowerShell-munkamenetet, amíg választ nem kap a felhőtől.</span><span class="sxs-lookup"><span data-stu-id="82fa8-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="82fa8-105">A PowerShell-feladatok lehetővé teszik, hogy egyetlen PowerShell-munkamenetből futtasson parancsmagokat a háttérben vagy végezzen egyszerre több feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="82fa8-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="82fa8-106">Ez a cikk rövid áttekintést nyújt az Azure PowerShell-parancsmagok PowerShell-feladatként való futtatásáról és annak ellenőrzéséről, hogy a feladatok befejeződtek-e.</span><span class="sxs-lookup"><span data-stu-id="82fa8-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="82fa8-107">A parancsok Azure PowerShellben való futtatásához Azure PowerShell-környezeteket kell használni, amelyekről részletesen [az Azure-környezeteket és a bejelentkezési hitelesítő adatokat](context-persistence.md) ismertető témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="82fa8-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="82fa8-108">További információ a PowerShell-feladatokról: [A PowerShell-feladatok ismertetése](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="82fa8-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="82fa8-109">Azure-környezetek és PowerShell-feladatok</span><span class="sxs-lookup"><span data-stu-id="82fa8-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="82fa8-110">A PowerShell-feladatok külön folyamatokként futnak, társított PowerShell-munkamenet nélkül, ezért meg kell osztani velük az Azure-beli hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="82fa8-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="82fa8-111">A rendszer Azure-beli környezeti objektumként, az alábbi módszerek valamelyikével adja át a hitelesítő adatokat:</span><span class="sxs-lookup"><span data-stu-id="82fa8-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="82fa8-112">Automatikus környezetmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="82fa8-112">Automatic context persistence.</span></span> <span data-ttu-id="82fa8-113">A környezetmegőrzés alapértelmezés szerint engedélyezve van, és több munkamenetre kiterjedően megőrzi a bejelentkezési adatokat.</span><span class="sxs-lookup"><span data-stu-id="82fa8-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="82fa8-114">Ha engedélyezve van a környezetmegőrzés, a rendszer átadja az aktuális Azure-környezetet az új folyamatnak:</span><span class="sxs-lookup"><span data-stu-id="82fa8-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="82fa8-115">Azure-beli környezeti objektum megadásához használja az `-AzContext` paramétert bármelyik Azure PowerShell-parancsmaggal:</span><span class="sxs-lookup"><span data-stu-id="82fa8-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="82fa8-116">Ha a környezetmegőrzés le van tiltva, meg kell adni az `-AzContext` argumentumot.</span><span class="sxs-lookup"><span data-stu-id="82fa8-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="82fa8-117">Használja az egyes Azure PowerShell-parancsmagok által biztosított `-AsJob` kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="82fa8-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="82fa8-118">Ez a kapcsoló automatikusan elindítja a parancsmagot PowerShell-feladatként, az aktív Azure-környezet használatával:</span><span class="sxs-lookup"><span data-stu-id="82fa8-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="82fa8-119">Ha ellenőrizni szeretné, hogy az adott parancsmag támogatja-e az `-AsJob` kapcsolót, tekintse meg a referenciadokumentációját.</span><span class="sxs-lookup"><span data-stu-id="82fa8-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="82fa8-120">Az `-AsJob` kapcsoló használatához nem kell engedélyezni a környezet automatikus mentését.</span><span class="sxs-lookup"><span data-stu-id="82fa8-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="82fa8-121">A futó feladatok állapotát a [Get-Job](/powershell/module/microsoft.powershell.core/get-job) parancsmaggal ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="82fa8-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="82fa8-122">Egy feladat pillanatnyi kimenetének lekéréséhez használja a [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="82fa8-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="82fa8-123">Ha távolról szeretné ellenőrizni egy művelet állapotát az Azure-on, használja a feladat által módosított erőforrás típusához társított `Get-` parancsmagokat:</span><span class="sxs-lookup"><span data-stu-id="82fa8-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="82fa8-124">Lásd még:</span><span class="sxs-lookup"><span data-stu-id="82fa8-124">See Also</span></span>

* [<span data-ttu-id="82fa8-125">Azure PowerShell-környezetek</span><span class="sxs-lookup"><span data-stu-id="82fa8-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="82fa8-126">A PowerShell-feladatok ismertetése</span><span class="sxs-lookup"><span data-stu-id="82fa8-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="82fa8-127">Get-Job referencia</span><span class="sxs-lookup"><span data-stu-id="82fa8-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="82fa8-128">Receive-Job referencia</span><span class="sxs-lookup"><span data-stu-id="82fa8-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
