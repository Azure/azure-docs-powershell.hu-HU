---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374259"
---
# <span data-ttu-id="9999f-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="9999f-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="9999f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9999f-102">SYNOPSIS</span></span>
<span data-ttu-id="9999f-103">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="9999f-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="9999f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9999f-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="9999f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9999f-105">DESCRIPTION</span></span>
<span data-ttu-id="9999f-106">Test-AzStackHCIConnection helyszíni csoportosított csomópontok és az Azure Stack HCI által megkövetelt Azure-szolgáltatások csatlakozását ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="9999f-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="9999f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9999f-107">EXAMPLES</span></span>

### <span data-ttu-id="9999f-108">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="9999f-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="9999f-109">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeedd</span><span class="sxs-lookup"><span data-stu-id="9999f-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="9999f-110">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="9999f-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="9999f-111">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="9999f-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="9999f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9999f-112">PARAMETERS</span></span>

### <span data-ttu-id="9999f-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9999f-113">-ComputerName</span></span>
<span data-ttu-id="9999f-114">Az Azure-ba regisztrált, a környezetben található fürtben található fürtcsomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9999f-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="9999f-115">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="9999f-115">-Credential</span></span>
<span data-ttu-id="9999f-116">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9999f-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="9999f-117">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9999f-117">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="9999f-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9999f-118">-EnvironmentName</span></span>
<span data-ttu-id="9999f-119">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9999f-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="9999f-120">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="9999f-120">Default is AzureCloud.</span></span>
<span data-ttu-id="9999f-121">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="9999f-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="9999f-122">-Régió</span><span class="sxs-lookup"><span data-stu-id="9999f-122">-Region</span></span>
<span data-ttu-id="9999f-123">Azt a régiót adja meg, amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="9999f-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="9999f-124">Nem használjuk, hacsak nem Canary régió.</span><span class="sxs-lookup"><span data-stu-id="9999f-124">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="9999f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9999f-125">CommonParameters</span></span>
<span data-ttu-id="9999f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9999f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9999f-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9999f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9999f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9999f-128">INPUTS</span></span>

## <span data-ttu-id="9999f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9999f-129">OUTPUTS</span></span>

### <span data-ttu-id="9999f-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="9999f-130">PSCustomObject.</span></span> <span data-ttu-id="9999f-131">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9999f-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="9999f-132">Teszt: Az elvégzett teszt neve.</span><span class="sxs-lookup"><span data-stu-id="9999f-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="9999f-133">EndpointTested: Endpoint used in the test.</span><span class="sxs-lookup"><span data-stu-id="9999f-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="9999f-134">IsRequired: True vagy False</span><span class="sxs-lookup"><span data-stu-id="9999f-134">IsRequired: True or False</span></span>
### <span data-ttu-id="9999f-135">Eredmény: Sikeres vagy Sikertelen</span><span class="sxs-lookup"><span data-stu-id="9999f-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="9999f-136">FailedNodes: Azon csomópontok listája, amelyeken a teszt sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="9999f-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="9999f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9999f-137">NOTES</span></span>

## <span data-ttu-id="9999f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9999f-138">RELATED LINKS</span></span>
