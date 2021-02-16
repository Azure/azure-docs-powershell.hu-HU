---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155459"
---
# <span data-ttu-id="74363-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="74363-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="74363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74363-102">SYNOPSIS</span></span>
<span data-ttu-id="74363-103">Felsorolja az összes vagy egy adott Automatikus Eszközkezelési IoT-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="74363-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="74363-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74363-104">SYNTAX</span></span>

### <span data-ttu-id="74363-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74363-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74363-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74363-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74363-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="74363-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74363-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74363-108">DESCRIPTION</span></span>
<span data-ttu-id="74363-109">Az IoT automatikus eszközkezelési konfigurációjának részletei vagy az IoT automatikus eszközkezelési konfigurációk listája az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="74363-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="74363-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="74363-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="74363-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74363-111">EXAMPLES</span></span>

### <span data-ttu-id="74363-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="74363-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="74363-113">Az IoT automatikus eszközkezelési konfigurációjának részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="74363-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="74363-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="74363-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="74363-115">Az IoT-központban listába sorolja fel az automatikus eszközkezelési konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="74363-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="74363-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74363-116">PARAMETERS</span></span>

### <span data-ttu-id="74363-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74363-117">-DefaultProfile</span></span>
<span data-ttu-id="74363-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74363-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74363-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74363-119">-InputObject</span></span>
<span data-ttu-id="74363-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="74363-120">IotHub object</span></span>

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

### <span data-ttu-id="74363-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="74363-121">-IotHubName</span></span>
<span data-ttu-id="74363-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="74363-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="74363-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74363-123">-Name</span></span>
<span data-ttu-id="74363-124">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="74363-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="74363-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74363-125">-ResourceGroupName</span></span>
<span data-ttu-id="74363-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="74363-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="74363-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74363-127">-ResourceId</span></span>
<span data-ttu-id="74363-128">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="74363-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="74363-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74363-129">CommonParameters</span></span>
<span data-ttu-id="74363-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74363-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74363-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74363-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74363-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74363-132">INPUTS</span></span>

### <span data-ttu-id="74363-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="74363-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="74363-134">System.String</span><span class="sxs-lookup"><span data-stu-id="74363-134">System.String</span></span>

## <span data-ttu-id="74363-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74363-135">OUTPUTS</span></span>

### <span data-ttu-id="74363-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="74363-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="74363-137">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="74363-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="74363-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74363-138">NOTES</span></span>

## <span data-ttu-id="74363-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74363-139">RELATED LINKS</span></span>
