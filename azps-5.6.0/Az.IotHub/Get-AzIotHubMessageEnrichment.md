---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936857"
---
# <span data-ttu-id="3753f-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3753f-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="3753f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3753f-102">SYNOPSIS</span></span>
<span data-ttu-id="3753f-103">Az IoT-központ üzenetgazdagítását vagy egy adott üzenetgazdagítást sorol fel.</span><span class="sxs-lookup"><span data-stu-id="3753f-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="3753f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3753f-104">SYNTAX</span></span>

### <span data-ttu-id="3753f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3753f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3753f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3753f-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3753f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3753f-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3753f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3753f-108">DESCRIPTION</span></span>
<span data-ttu-id="3753f-109">Az Azure IoT-központban az üzenetek gazdagításának részletes magyarázatát lásd: https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3753f-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3753f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3753f-110">EXAMPLES</span></span>

### <span data-ttu-id="3753f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3753f-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="3753f-112">List all message enrichments in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="3753f-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="3753f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3753f-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="3753f-114">Részletek megjelenítése az "újKulcs" üzenet gazdagításról.</span><span class="sxs-lookup"><span data-stu-id="3753f-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="3753f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3753f-115">PARAMETERS</span></span>

### <span data-ttu-id="3753f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3753f-116">-DefaultProfile</span></span>
<span data-ttu-id="3753f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3753f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3753f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3753f-118">-InputObject</span></span>
<span data-ttu-id="3753f-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3753f-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3753f-120">-Key</span><span class="sxs-lookup"><span data-stu-id="3753f-120">-Key</span></span>
<span data-ttu-id="3753f-121">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="3753f-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3753f-122">-Name</span></span>
<span data-ttu-id="3753f-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="3753f-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3753f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3753f-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3753f-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3753f-126">-ResourceId</span></span>
<span data-ttu-id="3753f-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3753f-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3753f-128">CommonParameters</span></span>
<span data-ttu-id="3753f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3753f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3753f-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3753f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3753f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3753f-131">INPUTS</span></span>

### <span data-ttu-id="3753f-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3753f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3753f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3753f-133">System.String</span></span>

## <span data-ttu-id="3753f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3753f-134">OUTPUTS</span></span>

### <span data-ttu-id="3753f-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3753f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="3753f-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="3753f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="3753f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3753f-137">NOTES</span></span>

## <span data-ttu-id="3753f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3753f-138">RELATED LINKS</span></span>
