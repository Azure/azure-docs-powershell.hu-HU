---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187761"
---
# <span data-ttu-id="5b705-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b705-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5b705-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b705-102">SYNOPSIS</span></span>
<span data-ttu-id="5b705-103">Felsorolja az automatikus eszközkezelés teljes konfigurációját vagy egy bizonyos IoT.</span><span class="sxs-lookup"><span data-stu-id="5b705-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="5b705-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b705-104">SYNTAX</span></span>

### <span data-ttu-id="5b705-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b705-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b705-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b705-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b705-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b705-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b705-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b705-108">DESCRIPTION</span></span>
<span data-ttu-id="5b705-109">Megtudhatja, hogy miként szerezhet be egy IoT automatikus eszközkezelés-konfiguráció vagy-lista IoT automatikus eszközkezelés-konfigurációját egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="5b705-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="5b705-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="5b705-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5b705-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5b705-111">EXAMPLES</span></span>

### <span data-ttu-id="5b705-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b705-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="5b705-113">Megtudhatja, hogy miként szerezhet be IoT automatikus eszközkezelés-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="5b705-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="5b705-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5b705-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="5b705-115">A lista IoT automatikus eszközkezelés-beállításai egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="5b705-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="5b705-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b705-116">PARAMETERS</span></span>

### <span data-ttu-id="5b705-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b705-117">-DefaultProfile</span></span>
<span data-ttu-id="5b705-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b705-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b705-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b705-119">-InputObject</span></span>
<span data-ttu-id="5b705-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5b705-120">IotHub object</span></span>

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

### <span data-ttu-id="5b705-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5b705-121">-IotHubName</span></span>
<span data-ttu-id="5b705-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="5b705-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5b705-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b705-123">-Name</span></span>
<span data-ttu-id="5b705-124">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b705-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5b705-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b705-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b705-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5b705-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b705-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b705-127">-ResourceId</span></span>
<span data-ttu-id="5b705-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5b705-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5b705-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b705-129">CommonParameters</span></span>
<span data-ttu-id="5b705-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b705-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b705-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b705-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b705-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b705-132">INPUTS</span></span>

### <span data-ttu-id="5b705-133">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5b705-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5b705-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5b705-134">System.String</span></span>

## <span data-ttu-id="5b705-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b705-135">OUTPUTS</span></span>

### <span data-ttu-id="5b705-136">Microsoft. Azure. Command. Management. IotHub. models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b705-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="5b705-137">Microsoft. Azure. Command. Management. IotHub. models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="5b705-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="5b705-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b705-138">NOTES</span></span>

## <span data-ttu-id="5b705-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b705-139">RELATED LINKS</span></span>