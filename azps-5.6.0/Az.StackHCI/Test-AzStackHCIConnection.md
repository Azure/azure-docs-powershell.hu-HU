---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930721"
---
# <span data-ttu-id="d17ab-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="d17ab-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="d17ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d17ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d17ab-103">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="d17ab-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="d17ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d17ab-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="d17ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d17ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d17ab-106">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="d17ab-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="d17ab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d17ab-107">EXAMPLES</span></span>

### <span data-ttu-id="d17ab-108">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="d17ab-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="d17ab-109">Invoking on one the cluster node.</span><span class="sxs-lookup"><span data-stu-id="d17ab-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="d17ab-110">Sikeres eset.</span><span class="sxs-lookup"><span data-stu-id="d17ab-110">Success case.</span></span>

### <span data-ttu-id="d17ab-111">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="d17ab-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="d17ab-112">Invoking on one the cluster node.</span><span class="sxs-lookup"><span data-stu-id="d17ab-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="d17ab-113">Sikertelen eset.</span><span class="sxs-lookup"><span data-stu-id="d17ab-113">Failed case.</span></span>

## <span data-ttu-id="d17ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d17ab-114">PARAMETERS</span></span>

### <span data-ttu-id="d17ab-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="d17ab-115">-ComputerName</span></span>
<span data-ttu-id="d17ab-116">Az Azure-ba regisztrált, a környezetben található fürtben található egyik fürtcsomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d17ab-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17ab-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="d17ab-117">-Credential</span></span>
<span data-ttu-id="d17ab-118">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d17ab-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="d17ab-119">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d17ab-119">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17ab-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d17ab-120">-EnvironmentName</span></span>
<span data-ttu-id="d17ab-121">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d17ab-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="d17ab-122">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="d17ab-122">Default is AzureCloud.</span></span>
<span data-ttu-id="d17ab-123">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="d17ab-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17ab-124">-Régió</span><span class="sxs-lookup"><span data-stu-id="d17ab-124">-Region</span></span>
<span data-ttu-id="d17ab-125">Azt a régiót adja meg, amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="d17ab-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="d17ab-126">Nem használjuk, hacsak nem Canary régió.</span><span class="sxs-lookup"><span data-stu-id="d17ab-126">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17ab-127">CommonParameters</span></span>
<span data-ttu-id="d17ab-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17ab-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d17ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17ab-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d17ab-130">INPUTS</span></span>

## <span data-ttu-id="d17ab-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d17ab-131">OUTPUTS</span></span>

### <span data-ttu-id="d17ab-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="d17ab-132">PSCustomObject.</span></span> <span data-ttu-id="d17ab-133">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d17ab-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="d17ab-134">Teszt: Az elvégzett teszt neve.</span><span class="sxs-lookup"><span data-stu-id="d17ab-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="d17ab-135">EndpointTested: Endpoint used in the test.</span><span class="sxs-lookup"><span data-stu-id="d17ab-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="d17ab-136">IsRequired: True vagy False</span><span class="sxs-lookup"><span data-stu-id="d17ab-136">IsRequired: True or False</span></span>
### <span data-ttu-id="d17ab-137">Eredmény: Sikeres vagy Sikertelen</span><span class="sxs-lookup"><span data-stu-id="d17ab-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="d17ab-138">FailedNodes: Azon csomópontok listája, amelyeken a teszt sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="d17ab-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="d17ab-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d17ab-139">NOTES</span></span>

## <span data-ttu-id="d17ab-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d17ab-140">RELATED LINKS</span></span>
