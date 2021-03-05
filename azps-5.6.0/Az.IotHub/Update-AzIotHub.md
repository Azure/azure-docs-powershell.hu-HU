---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: b7b89f239949f6a61e3388b0f5cb794cd4ad0c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004069"
---
# <span data-ttu-id="7cf50-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="7cf50-101">Update-AzIotHub</span></span>

## <span data-ttu-id="7cf50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf50-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf50-103">Frissítsen egy Azure IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="7cf50-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="7cf50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cf50-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cf50-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf50-106">Frissítheti az IotHubok címketulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7cf50-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="7cf50-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cf50-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf50-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7cf50-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="7cf50-109">Frissítse egy IoT-központ címkéit.</span><span class="sxs-lookup"><span data-stu-id="7cf50-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="7cf50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf50-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf50-111">-DefaultProfile</span></span>
<span data-ttu-id="7cf50-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cf50-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf50-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7cf50-113">-Name</span></span>
<span data-ttu-id="7cf50-114">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="7cf50-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="7cf50-115">-Reset</span></span>
<span data-ttu-id="7cf50-116">IoTHub-címkék alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="7cf50-116">Reset IoTHub Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf50-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cf50-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7cf50-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cf50-119">-Tag</span></span>
<span data-ttu-id="7cf50-120">IoTHub címkegyűjtemény</span><span class="sxs-lookup"><span data-stu-id="7cf50-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf50-121">-Confirm</span></span>
<span data-ttu-id="7cf50-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7cf50-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf50-123">-WhatIf</span></span>
<span data-ttu-id="7cf50-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7cf50-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf50-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cf50-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf50-126">CommonParameters</span></span>
<span data-ttu-id="7cf50-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf50-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf50-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf50-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf50-129">INPUTS</span></span>

### <span data-ttu-id="7cf50-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf50-130">System.String</span></span>

## <span data-ttu-id="7cf50-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cf50-131">OUTPUTS</span></span>

### <span data-ttu-id="7cf50-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7cf50-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="7cf50-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cf50-133">NOTES</span></span>

## <span data-ttu-id="7cf50-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cf50-134">RELATED LINKS</span></span>
