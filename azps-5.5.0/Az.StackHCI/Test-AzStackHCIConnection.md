---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145498"
---
# <span data-ttu-id="31b14-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="31b14-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="31b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b14-102">SYNOPSIS</span></span>
<span data-ttu-id="31b14-103">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="31b14-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="31b14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31b14-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="31b14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31b14-105">DESCRIPTION</span></span>
<span data-ttu-id="31b14-106">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="31b14-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="31b14-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31b14-107">EXAMPLES</span></span>

### <span data-ttu-id="31b14-108">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="31b14-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="31b14-109">Invoking on one the cluster node.</span><span class="sxs-lookup"><span data-stu-id="31b14-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="31b14-110">Sikeres eset.</span><span class="sxs-lookup"><span data-stu-id="31b14-110">Success case.</span></span>

### <span data-ttu-id="31b14-111">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="31b14-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="31b14-112">Invoking on one the cluster node.</span><span class="sxs-lookup"><span data-stu-id="31b14-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="31b14-113">Sikertelen eset.</span><span class="sxs-lookup"><span data-stu-id="31b14-113">Failed case.</span></span>

## <span data-ttu-id="31b14-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b14-114">PARAMETERS</span></span>

### <span data-ttu-id="31b14-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="31b14-115">-ComputerName</span></span>
<span data-ttu-id="31b14-116">Az Azure-ba regisztrált, a környezetben található fürtben található fürtcsomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="31b14-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="31b14-117">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="31b14-117">-Credential</span></span>
<span data-ttu-id="31b14-118">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="31b14-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="31b14-119">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="31b14-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="31b14-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="31b14-120">-EnvironmentName</span></span>
<span data-ttu-id="31b14-121">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="31b14-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="31b14-122">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="31b14-122">Default is AzureCloud.</span></span>
<span data-ttu-id="31b14-123">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="31b14-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="31b14-124">-Régió</span><span class="sxs-lookup"><span data-stu-id="31b14-124">-Region</span></span>
<span data-ttu-id="31b14-125">Azt a régiót adja meg, amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="31b14-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="31b14-126">Csak akkor használja, ha a Canary régió.</span><span class="sxs-lookup"><span data-stu-id="31b14-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="31b14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b14-127">CommonParameters</span></span>
<span data-ttu-id="31b14-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b14-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31b14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b14-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31b14-130">INPUTS</span></span>

## <span data-ttu-id="31b14-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31b14-131">OUTPUTS</span></span>

### <span data-ttu-id="31b14-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="31b14-132">PSCustomObject.</span></span> <span data-ttu-id="31b14-133">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="31b14-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="31b14-134">Teszt: Az elvégzett teszt neve.</span><span class="sxs-lookup"><span data-stu-id="31b14-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="31b14-135">EndpointTested: Endpoint used in the test.</span><span class="sxs-lookup"><span data-stu-id="31b14-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="31b14-136">IsRequired: True vagy False</span><span class="sxs-lookup"><span data-stu-id="31b14-136">IsRequired: True or False</span></span>
### <span data-ttu-id="31b14-137">Eredmény: Sikeres vagy Sikertelen</span><span class="sxs-lookup"><span data-stu-id="31b14-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="31b14-138">FailedNodes: Azon csomópontok listája, amelyeken a teszt sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="31b14-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="31b14-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31b14-139">NOTES</span></span>

## <span data-ttu-id="31b14-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31b14-140">RELATED LINKS</span></span>
