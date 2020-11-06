---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
ms.openlocfilehash: 51c2772a891cf39ba780c6ff3da0af40170f477e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492737"
---
# <span data-ttu-id="d13e8-101">Get-AzureRmSecurityTask</span><span class="sxs-lookup"><span data-stu-id="d13e8-101">Get-AzureRmSecurityTask</span></span>

## <span data-ttu-id="d13e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d13e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d13e8-103">Az Azure Security Center által a biztonsági testtartás megerősítéséhez javasolt biztonsági feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d13e8-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d13e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d13e8-104">SYNTAX</span></span>

### <span data-ttu-id="d13e8-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d13e8-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d13e8-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d13e8-106">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d13e8-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d13e8-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d13e8-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d13e8-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d13e8-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d13e8-109">ResourceId</span></span>
```
Get-AzureRmSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d13e8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="d13e8-110">DESCRIPTION</span></span>
<span data-ttu-id="d13e8-111">Az Azure Security Center a potenciális biztonsági problémák felderítéséhez beolvassa az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="d13e8-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="d13e8-112">Ezzel a parancsmaggal felfedezheti az Azure Security Center által javasolt biztonsági feladatokat.</span><span class="sxs-lookup"><span data-stu-id="d13e8-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="d13e8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d13e8-113">EXAMPLES</span></span>

### <span data-ttu-id="d13e8-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d13e8-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="d13e8-115">Az előfizetésben szereplő erőforrásokban felfedezett összes biztonsági feladatot megkapja.</span><span class="sxs-lookup"><span data-stu-id="d13e8-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="d13e8-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d13e8-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="d13e8-117">Az erőforrás-csoporton belüli erőforrásokban észlelt összes biztonsági feladatot beolvassa.</span><span class="sxs-lookup"><span data-stu-id="d13e8-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="d13e8-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="d13e8-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="d13e8-119">Meghatározott biztonsági feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="d13e8-119">Gets a specific security task.</span></span>

## <span data-ttu-id="d13e8-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d13e8-120">PARAMETERS</span></span>

### <span data-ttu-id="d13e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13e8-121">-DefaultProfile</span></span>
<span data-ttu-id="d13e8-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d13e8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13e8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d13e8-123">-Name</span></span>
<span data-ttu-id="d13e8-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d13e8-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="d13e8-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d13e8-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13e8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d13e8-127">-ResourceId</span></span>
<span data-ttu-id="d13e8-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d13e8-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13e8-129">CommonParameters</span></span>
<span data-ttu-id="d13e8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d13e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13e8-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13e8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13e8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d13e8-132">INPUTS</span></span>

### <span data-ttu-id="d13e8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d13e8-133">System.String</span></span>

## <span data-ttu-id="d13e8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d13e8-134">OUTPUTS</span></span>

### <span data-ttu-id="d13e8-135">Microsoft. Azure. commands. Security. models. Tasks. PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="d13e8-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="d13e8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d13e8-136">NOTES</span></span>

## <span data-ttu-id="d13e8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d13e8-137">RELATED LINKS</span></span>
