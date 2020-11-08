---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195990"
---
# <span data-ttu-id="3ca0a-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3ca0a-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="3ca0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ca0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca0a-103">IoT-os Device Module-modult kap.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="3ca0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ca0a-104">SYNTAX</span></span>

### <span data-ttu-id="3ca0a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ca0a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ca0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ca0a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca0a-109">IoT-os Device Module-modult kap.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="3ca0a-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="3ca0a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3ca0a-111">EXAMPLES</span></span>

### <span data-ttu-id="3ca0a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ca0a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="3ca0a-113">Az Device Module Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="3ca0a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ca0a-114">PARAMETERS</span></span>

### <span data-ttu-id="3ca0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0a-115">-DefaultProfile</span></span>
<span data-ttu-id="3ca0a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca0a-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3ca0a-117">-DeviceId</span></span>
<span data-ttu-id="3ca0a-118">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-118">Target Device Id.</span></span>

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

### <span data-ttu-id="3ca0a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca0a-119">-InputObject</span></span>
<span data-ttu-id="3ca0a-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3ca0a-120">IotHub object</span></span>

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

### <span data-ttu-id="3ca0a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3ca0a-121">-IotHubName</span></span>
<span data-ttu-id="3ca0a-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="3ca0a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3ca0a-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="3ca0a-123">-ModuleId</span></span>
<span data-ttu-id="3ca0a-124">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="3ca0a-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ca0a-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3ca0a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3ca0a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca0a-127">-ResourceId</span></span>
<span data-ttu-id="3ca0a-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3ca0a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3ca0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca0a-129">CommonParameters</span></span>
<span data-ttu-id="3ca0a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ca0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca0a-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca0a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca0a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca0a-132">INPUTS</span></span>

### <span data-ttu-id="3ca0a-133">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3ca0a-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3ca0a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca0a-134">System.String</span></span>

## <span data-ttu-id="3ca0a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca0a-135">OUTPUTS</span></span>

### <span data-ttu-id="3ca0a-136">Microsoft. Azure. Command. Management. IotHub. models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3ca0a-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="3ca0a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ca0a-137">NOTES</span></span>

## <span data-ttu-id="3ca0a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ca0a-138">RELATED LINKS</span></span>
