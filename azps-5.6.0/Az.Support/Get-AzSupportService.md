---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: bb5bb20439aa1112638cdd0ab61f12976cfd3a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928858"
---
# <span data-ttu-id="853c1-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="853c1-101">Get-AzSupportService</span></span>

## <span data-ttu-id="853c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="853c1-102">SYNOPSIS</span></span>
<span data-ttu-id="853c1-103">Olyan szolgáltatások érhetők el, amelyekhez támogatás áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="853c1-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="853c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="853c1-104">SYNTAX</span></span>

### <span data-ttu-id="853c1-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="853c1-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="853c1-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="853c1-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="853c1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="853c1-107">DESCRIPTION</span></span>
<span data-ttu-id="853c1-108">Azon Azure-szolgáltatások aktuális listáját tartalmazza, amelyekhez elérhető a támogatás.</span><span class="sxs-lookup"><span data-stu-id="853c1-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="853c1-109">Minden szolgáltatás egy vagy több Azure erőforrás-kezelőt (ARM) tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="853c1-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="853c1-110">Az erőforrástípusok (például: 'microsoft.compute/virtualmachines') hasznosak lehetnek a megfelelő termék- és ARM leképezésében technikai támogatási jegy létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="853c1-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="853c1-111">Mindegyik Azure-szolgáltatás saját kategóriákkal, úgynevezett problémabesorolással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="853c1-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="853c1-112">A Szolgáltatás problémabesorolásának aktuális listája a Get-AzSupportProblemClassification segítségével.</span><span class="sxs-lookup"><span data-stu-id="853c1-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="853c1-113">A szolgáltatás- és problémabesorolás GUID azonosítóját használva létrehozhat egy új támogatási jegyet a New-AzSupportTicket használatával.</span><span class="sxs-lookup"><span data-stu-id="853c1-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="853c1-114">Mindig a programozással beszerezhető GUID azonosítókat használja a szolgáltatás- és problémabesorolási GUID azonosítókhoz.</span><span class="sxs-lookup"><span data-stu-id="853c1-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="853c1-115">Ezzel a gyakorlattal biztosíthatja, hogy a támogatási jegy létrehozásához a legújabb szolgáltatás- és problémabesorolási GUID azonosítókat tudja beállítani.</span><span class="sxs-lookup"><span data-stu-id="853c1-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="853c1-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="853c1-116">EXAMPLES</span></span>

### <span data-ttu-id="853c1-117">1. példa: Az összes szolgáltatás elérhetővé válik támogatásra</span><span class="sxs-lookup"><span data-stu-id="853c1-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="853c1-118">2. példa: Egyetlen szolgáltatás részleteinek megtekintése támogatásra elérhető azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="853c1-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="853c1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="853c1-119">PARAMETERS</span></span>

### <span data-ttu-id="853c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="853c1-120">-DefaultProfile</span></span>
<span data-ttu-id="853c1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="853c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853c1-122">-Id</span><span class="sxs-lookup"><span data-stu-id="853c1-122">-Id</span></span>
<span data-ttu-id="853c1-123">Szolgáltatásazonosító.</span><span class="sxs-lookup"><span data-stu-id="853c1-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853c1-124">CommonParameters</span></span>
<span data-ttu-id="853c1-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="853c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853c1-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="853c1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853c1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="853c1-127">INPUTS</span></span>

### <span data-ttu-id="853c1-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="853c1-128">None</span></span>

## <span data-ttu-id="853c1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="853c1-129">OUTPUTS</span></span>

### <span data-ttu-id="853c1-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="853c1-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="853c1-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="853c1-131">NOTES</span></span>

## <span data-ttu-id="853c1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="853c1-132">RELATED LINKS</span></span>
