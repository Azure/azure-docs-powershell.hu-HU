---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 6c47e2de9a234d5ae52598002d2ec5db93748692
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666271"
---
# <span data-ttu-id="fd7e7-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fd7e7-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="fd7e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e7-103">Felsorolja az összes üzenet dúsítását, vagy az IoT-hub adott üzenet dúsítását.</span><span class="sxs-lookup"><span data-stu-id="fd7e7-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="fd7e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd7e7-104">SYNTAX</span></span>

### <span data-ttu-id="fd7e7-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd7e7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7e7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd7e7-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7e7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd7e7-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd7e7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd7e7-108">DESCRIPTION</span></span>
<span data-ttu-id="fd7e7-109">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="fd7e7-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="fd7e7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd7e7-110">EXAMPLES</span></span>

### <span data-ttu-id="fd7e7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd7e7-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="fd7e7-112">Az összes üzenet dúsításának listázása az MyIotHub-on</span><span class="sxs-lookup"><span data-stu-id="fd7e7-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="fd7e7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd7e7-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="fd7e7-114">A "newKey" üzenet gazdagodás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="fd7e7-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="fd7e7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd7e7-115">PARAMETERS</span></span>

### <span data-ttu-id="fd7e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e7-116">-DefaultProfile</span></span>
<span data-ttu-id="fd7e7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd7e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7e7-118">-InputObject</span></span>
<span data-ttu-id="fd7e7-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="fd7e7-119">IotHub object</span></span>

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

### <span data-ttu-id="fd7e7-120">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="fd7e7-120">-Key</span></span>
<span data-ttu-id="fd7e7-121">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="fd7e7-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="fd7e7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd7e7-122">-Name</span></span>
<span data-ttu-id="fd7e7-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="fd7e7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd7e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e7-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fd7e7-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd7e7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7e7-126">-ResourceId</span></span>
<span data-ttu-id="fd7e7-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fd7e7-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fd7e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e7-128">CommonParameters</span></span>
<span data-ttu-id="fd7e7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd7e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7e7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7e7-131">INPUTS</span></span>

### <span data-ttu-id="fd7e7-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fd7e7-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fd7e7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7e7-133">System.String</span></span>

## <span data-ttu-id="fd7e7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7e7-134">OUTPUTS</span></span>

### <span data-ttu-id="fd7e7-135">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="fd7e7-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="fd7e7-136">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="fd7e7-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="fd7e7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd7e7-137">NOTES</span></span>

## <span data-ttu-id="fd7e7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd7e7-138">RELATED LINKS</span></span>
