---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386425"
---
# <span data-ttu-id="dcb8f-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="dcb8f-101">Update-AzIotHub</span></span>

## <span data-ttu-id="dcb8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb8f-103">Frissítsen egy Azure IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="dcb8f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcb8f-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcb8f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcb8f-105">DESCRIPTION</span></span>
<span data-ttu-id="dcb8f-106">Frissítheti az IotHubok címketulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="dcb8f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcb8f-107">EXAMPLES</span></span>

### <span data-ttu-id="dcb8f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dcb8f-108">Example 1</span></span>
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

<span data-ttu-id="dcb8f-109">Frissítse egy IoT-központ címkéit.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="dcb8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcb8f-110">PARAMETERS</span></span>

### <span data-ttu-id="dcb8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb8f-111">-DefaultProfile</span></span>
<span data-ttu-id="dcb8f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcb8f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dcb8f-113">-Name</span></span>
<span data-ttu-id="dcb8f-114">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="dcb8f-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dcb8f-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="dcb8f-115">-Reset</span></span>
<span data-ttu-id="dcb8f-116">IoTHub-címkék alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="dcb8f-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="dcb8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcb8f-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dcb8f-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dcb8f-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="dcb8f-119">-Tag</span></span>
<span data-ttu-id="dcb8f-120">IoTHub címkegyűjtemény</span><span class="sxs-lookup"><span data-stu-id="dcb8f-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="dcb8f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcb8f-121">-Confirm</span></span>
<span data-ttu-id="dcb8f-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcb8f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb8f-123">-WhatIf</span></span>
<span data-ttu-id="dcb8f-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb8f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcb8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb8f-126">CommonParameters</span></span>
<span data-ttu-id="dcb8f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb8f-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb8f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb8f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcb8f-129">INPUTS</span></span>

### <span data-ttu-id="dcb8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dcb8f-130">System.String</span></span>

## <span data-ttu-id="dcb8f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcb8f-131">OUTPUTS</span></span>

### <span data-ttu-id="dcb8f-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dcb8f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="dcb8f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcb8f-133">NOTES</span></span>

## <span data-ttu-id="dcb8f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcb8f-134">RELATED LINKS</span></span>
