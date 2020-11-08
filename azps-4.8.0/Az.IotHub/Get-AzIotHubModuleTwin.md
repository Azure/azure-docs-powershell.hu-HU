---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182741"
---
# <span data-ttu-id="f7cba-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f7cba-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="f7cba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7cba-102">SYNOPSIS</span></span>
<span data-ttu-id="f7cba-103">IoT-os Device Module-modult kap.</span><span class="sxs-lookup"><span data-stu-id="f7cba-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="f7cba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7cba-104">SYNTAX</span></span>

### <span data-ttu-id="f7cba-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7cba-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7cba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7cba-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7cba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f7cba-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7cba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7cba-108">DESCRIPTION</span></span>
<span data-ttu-id="f7cba-109">IoT-os Device Module-modult kap.</span><span class="sxs-lookup"><span data-stu-id="f7cba-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="f7cba-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="f7cba-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="f7cba-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f7cba-111">EXAMPLES</span></span>

### <span data-ttu-id="f7cba-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7cba-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="f7cba-113">Az Device Module Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f7cba-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="f7cba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7cba-114">PARAMETERS</span></span>

### <span data-ttu-id="f7cba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7cba-115">-DefaultProfile</span></span>
<span data-ttu-id="f7cba-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7cba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7cba-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f7cba-117">-DeviceId</span></span>
<span data-ttu-id="f7cba-118">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f7cba-118">Target Device Id.</span></span>

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

### <span data-ttu-id="f7cba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7cba-119">-InputObject</span></span>
<span data-ttu-id="f7cba-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="f7cba-120">IotHub object</span></span>

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

### <span data-ttu-id="f7cba-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f7cba-121">-IotHubName</span></span>
<span data-ttu-id="f7cba-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="f7cba-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f7cba-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f7cba-123">-ModuleId</span></span>
<span data-ttu-id="f7cba-124">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="f7cba-124">Target Module Id.</span></span>

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

### <span data-ttu-id="f7cba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7cba-125">-ResourceGroupName</span></span>
<span data-ttu-id="f7cba-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f7cba-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f7cba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7cba-127">-ResourceId</span></span>
<span data-ttu-id="f7cba-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f7cba-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f7cba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7cba-129">CommonParameters</span></span>
<span data-ttu-id="f7cba-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7cba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7cba-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7cba-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7cba-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cba-132">INPUTS</span></span>

### <span data-ttu-id="f7cba-133">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f7cba-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f7cba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f7cba-134">System.String</span></span>

## <span data-ttu-id="f7cba-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cba-135">OUTPUTS</span></span>

### <span data-ttu-id="f7cba-136">Microsoft. Azure. Command. Management. IotHub. models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f7cba-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="f7cba-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7cba-137">NOTES</span></span>

## <span data-ttu-id="f7cba-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7cba-138">RELATED LINKS</span></span>
