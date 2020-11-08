---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195997"
---
# <span data-ttu-id="cd668-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd668-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="cd668-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd668-102">SYNOPSIS</span></span>
<span data-ttu-id="cd668-103">Felsorolja az összes üzenet dúsítását, vagy az IoT-hub adott üzenet dúsítását.</span><span class="sxs-lookup"><span data-stu-id="cd668-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="cd668-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd668-104">SYNTAX</span></span>

### <span data-ttu-id="cd668-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd668-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd668-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd668-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd668-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd668-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd668-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd668-108">DESCRIPTION</span></span>
<span data-ttu-id="cd668-109">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="cd668-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="cd668-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cd668-110">EXAMPLES</span></span>

### <span data-ttu-id="cd668-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd668-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="cd668-112">Az összes üzenet dúsításának listázása az MyIotHub-on</span><span class="sxs-lookup"><span data-stu-id="cd668-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="cd668-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cd668-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="cd668-114">A "newKey" üzenet gazdagodás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cd668-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="cd668-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd668-115">PARAMETERS</span></span>

### <span data-ttu-id="cd668-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd668-116">-DefaultProfile</span></span>
<span data-ttu-id="cd668-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd668-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd668-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd668-118">-InputObject</span></span>
<span data-ttu-id="cd668-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="cd668-119">IotHub object</span></span>

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

### <span data-ttu-id="cd668-120">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="cd668-120">-Key</span></span>
<span data-ttu-id="cd668-121">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="cd668-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="cd668-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd668-122">-Name</span></span>
<span data-ttu-id="cd668-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="cd668-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cd668-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd668-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd668-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cd668-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cd668-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd668-126">-ResourceId</span></span>
<span data-ttu-id="cd668-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cd668-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd668-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd668-128">CommonParameters</span></span>
<span data-ttu-id="cd668-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd668-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd668-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd668-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd668-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd668-131">INPUTS</span></span>

### <span data-ttu-id="cd668-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cd668-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cd668-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd668-133">System.String</span></span>

## <span data-ttu-id="cd668-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd668-134">OUTPUTS</span></span>

### <span data-ttu-id="cd668-135">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="cd668-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="cd668-136">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="cd668-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="cd668-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd668-137">NOTES</span></span>

## <span data-ttu-id="cd668-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd668-138">RELATED LINKS</span></span>
