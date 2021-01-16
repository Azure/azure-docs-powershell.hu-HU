---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480147"
---
# <span data-ttu-id="0c997-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="0c997-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="0c997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c997-102">SYNOPSIS</span></span>
<span data-ttu-id="0c997-103">Egy IoT-eszközmodul modult kap.</span><span class="sxs-lookup"><span data-stu-id="0c997-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="0c997-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c997-104">SYNTAX</span></span>

### <span data-ttu-id="0c997-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c997-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c997-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c997-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c997-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0c997-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c997-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c997-108">DESCRIPTION</span></span>
<span data-ttu-id="0c997-109">Egy IoT-eszközmodul modult kap.</span><span class="sxs-lookup"><span data-stu-id="0c997-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="0c997-110">További https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="0c997-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="0c997-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c997-111">EXAMPLES</span></span>

### <span data-ttu-id="0c997-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0c997-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="0c997-113">Az eszközmodul modul objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0c997-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="0c997-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c997-114">PARAMETERS</span></span>

### <span data-ttu-id="0c997-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c997-115">-DefaultProfile</span></span>
<span data-ttu-id="0c997-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c997-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c997-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0c997-117">-DeviceId</span></span>
<span data-ttu-id="0c997-118">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c997-118">Target Device Id.</span></span>

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

### <span data-ttu-id="0c997-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c997-119">-InputObject</span></span>
<span data-ttu-id="0c997-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="0c997-120">IotHub object</span></span>

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

### <span data-ttu-id="0c997-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0c997-121">-IotHubName</span></span>
<span data-ttu-id="0c997-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="0c997-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0c997-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="0c997-123">-ModuleId</span></span>
<span data-ttu-id="0c997-124">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0c997-124">Target Module Id.</span></span>

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

### <span data-ttu-id="0c997-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c997-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c997-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0c997-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0c997-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c997-127">-ResourceId</span></span>
<span data-ttu-id="0c997-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0c997-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0c997-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c997-129">CommonParameters</span></span>
<span data-ttu-id="0c997-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c997-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c997-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c997-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c997-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c997-132">INPUTS</span></span>

### <span data-ttu-id="0c997-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0c997-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0c997-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0c997-134">System.String</span></span>

## <span data-ttu-id="0c997-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c997-135">OUTPUTS</span></span>

### <span data-ttu-id="0c997-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="0c997-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="0c997-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c997-137">NOTES</span></span>

## <span data-ttu-id="0c997-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c997-138">RELATED LINKS</span></span>
