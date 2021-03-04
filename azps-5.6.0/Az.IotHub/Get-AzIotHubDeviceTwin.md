---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936890"
---
# <span data-ttu-id="c28cf-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="c28cf-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="c28cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c28cf-103">Eszközeszközt kap.</span><span class="sxs-lookup"><span data-stu-id="c28cf-103">Gets a device twin.</span></span>

## <span data-ttu-id="c28cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c28cf-104">SYNTAX</span></span>

### <span data-ttu-id="c28cf-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c28cf-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c28cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c28cf-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c28cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c28cf-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c28cf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c28cf-108">DESCRIPTION</span></span>
<span data-ttu-id="c28cf-109">Eszközeszközt kap.</span><span class="sxs-lookup"><span data-stu-id="c28cf-109">Gets a device twin.</span></span> <span data-ttu-id="c28cf-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="c28cf-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="c28cf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c28cf-111">EXAMPLES</span></span>

### <span data-ttu-id="c28cf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c28cf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="c28cf-113">Az eszköz objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c28cf-113">Returns the device twin object.</span></span>

## <span data-ttu-id="c28cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28cf-114">PARAMETERS</span></span>

### <span data-ttu-id="c28cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28cf-115">-DefaultProfile</span></span>
<span data-ttu-id="c28cf-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c28cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28cf-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c28cf-117">-DeviceId</span></span>
<span data-ttu-id="c28cf-118">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c28cf-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c28cf-119">-InputObject</span></span>
<span data-ttu-id="c28cf-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c28cf-120">IotHub object</span></span>

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

### <span data-ttu-id="c28cf-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c28cf-121">-IotHubName</span></span>
<span data-ttu-id="c28cf-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="c28cf-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c28cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="c28cf-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c28cf-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c28cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c28cf-125">-ResourceId</span></span>
<span data-ttu-id="c28cf-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c28cf-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c28cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28cf-127">CommonParameters</span></span>
<span data-ttu-id="c28cf-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28cf-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c28cf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28cf-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c28cf-130">INPUTS</span></span>

### <span data-ttu-id="c28cf-131">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c28cf-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c28cf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c28cf-132">System.String</span></span>

## <span data-ttu-id="c28cf-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28cf-133">OUTPUTS</span></span>

### <span data-ttu-id="c28cf-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="c28cf-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="c28cf-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c28cf-135">NOTES</span></span>

## <span data-ttu-id="c28cf-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c28cf-136">RELATED LINKS</span></span>
