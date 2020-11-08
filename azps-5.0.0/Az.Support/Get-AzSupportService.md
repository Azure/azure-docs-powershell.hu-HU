---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186325"
---
# <span data-ttu-id="4d8c4-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="4d8c4-101">Get-AzSupportService</span></span>

## <span data-ttu-id="4d8c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8c4-103">Olyan szolgáltatások beszerzése, amelyekhez támogatás érhető el.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="4d8c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d8c4-104">SYNTAX</span></span>

### <span data-ttu-id="4d8c4-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d8c4-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d8c4-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8c4-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d8c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d8c4-107">DESCRIPTION</span></span>
<span data-ttu-id="4d8c4-108">Beolvassa az Azure Services jelenlegi listáját, amelyhez támogatás érhető el.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="4d8c4-109">Az egyes szolgáltatások tartalmazhatnak egy vagy több Azure Resource Manager (ARM) erőforrás-típus adatait.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="4d8c4-110">Erőforrástípusok (példa: "Microsoft. számítási/virtualmachines") akkor lehet hasznos, ha egy műszaki támogatási jegy létrehozásakor a megfelelő terméket és ARM erőforrást meg szeretné feleltetni.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="4d8c4-111">Minden Azure-szolgáltatáshoz tartozik saját kategóriák a probléma besorolásához.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="4d8c4-112">Bemutatjuk a szolgáltatás problémás besorolásának aktuális listáját a Get-AzSupportProblemClassification segítségével.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="4d8c4-113">A szolgáltatás és a probléma besorolása GLOBÁLISan új támogatási jegyet hozhat létre a New-AzSupportTicket segítségével.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="4d8c4-114">Mindig használja a szolgáltatás-és probléma-besorolási GUID-azonosítókat, amelyek programozottan szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="4d8c4-115">Ez a gyakorlat biztosítja, hogy a menetjegy-teremtéshez legutóbb használt szolgáltatási és probléma-besorolási GUID-azonosítók legyenek.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="4d8c4-116">Példák</span><span class="sxs-lookup"><span data-stu-id="4d8c4-116">EXAMPLES</span></span>

### <span data-ttu-id="4d8c4-117">Példa 1: támogatás kérése az összes szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="4d8c4-117">Example 1: Get all services available for support</span></span>
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

### <span data-ttu-id="4d8c4-118">2. példa: az egyetlen szolgáltatás részleteinek megjelenítése a támogatáshoz elérhető azonosítóval</span><span class="sxs-lookup"><span data-stu-id="4d8c4-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="4d8c4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d8c4-119">PARAMETERS</span></span>

### <span data-ttu-id="4d8c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8c4-120">-DefaultProfile</span></span>
<span data-ttu-id="4d8c4-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d8c4-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4d8c4-122">-Id</span></span>
<span data-ttu-id="4d8c4-123">Szolgáltatás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-123">Service id.</span></span>

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

### <span data-ttu-id="4d8c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8c4-124">CommonParameters</span></span>
<span data-ttu-id="4d8c4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d8c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8c4-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d8c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8c4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d8c4-127">INPUTS</span></span>

### <span data-ttu-id="4d8c4-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="4d8c4-128">None</span></span>

## <span data-ttu-id="4d8c4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d8c4-129">OUTPUTS</span></span>

### <span data-ttu-id="4d8c4-130">Microsoft. Azure. commands. support. models. PSSupportService</span><span class="sxs-lookup"><span data-stu-id="4d8c4-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="4d8c4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d8c4-131">NOTES</span></span>

## <span data-ttu-id="4d8c4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d8c4-132">RELATED LINKS</span></span>
