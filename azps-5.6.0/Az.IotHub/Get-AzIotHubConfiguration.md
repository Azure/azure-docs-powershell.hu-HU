---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936945"
---
# <span data-ttu-id="cdfd5-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdfd5-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="cdfd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfd5-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfd5-103">Felsorolja az összes vagy egy adott Automatikus Eszközkezelési IoT-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="cdfd5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cdfd5-104">SYNTAX</span></span>

### <span data-ttu-id="cdfd5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdfd5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdfd5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdfd5-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdfd5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdfd5-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdfd5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cdfd5-108">DESCRIPTION</span></span>
<span data-ttu-id="cdfd5-109">Az IoT automatikus eszközkezelési konfigurációjának részletei, illetve az IoT automatikus eszközkezelési konfigurációjának listája az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="cdfd5-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="cdfd5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cdfd5-111">EXAMPLES</span></span>

### <span data-ttu-id="cdfd5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="cdfd5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="cdfd5-113">Az IoT automatikus eszközkezelési konfigurációjának részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="cdfd5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cdfd5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="cdfd5-115">Az IoT-központban felsorolja az automatikus eszközkezelési konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="cdfd5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdfd5-116">PARAMETERS</span></span>

### <span data-ttu-id="cdfd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfd5-117">-DefaultProfile</span></span>
<span data-ttu-id="cdfd5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdfd5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdfd5-119">-InputObject</span></span>
<span data-ttu-id="cdfd5-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="cdfd5-120">IotHub object</span></span>

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

### <span data-ttu-id="cdfd5-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cdfd5-121">-IotHubName</span></span>
<span data-ttu-id="cdfd5-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="cdfd5-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cdfd5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cdfd5-123">-Name</span></span>
<span data-ttu-id="cdfd5-124">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="cdfd5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfd5-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdfd5-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cdfd5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cdfd5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdfd5-127">-ResourceId</span></span>
<span data-ttu-id="cdfd5-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cdfd5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cdfd5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfd5-129">CommonParameters</span></span>
<span data-ttu-id="cdfd5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfd5-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfd5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfd5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdfd5-132">INPUTS</span></span>

### <span data-ttu-id="cdfd5-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cdfd5-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cdfd5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cdfd5-134">System.String</span></span>

## <span data-ttu-id="cdfd5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdfd5-135">OUTPUTS</span></span>

### <span data-ttu-id="cdfd5-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdfd5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="cdfd5-137">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="cdfd5-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="cdfd5-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cdfd5-138">NOTES</span></span>

## <span data-ttu-id="cdfd5-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdfd5-139">RELATED LINKS</span></span>
