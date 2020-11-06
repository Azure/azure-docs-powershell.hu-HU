---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492528"
---
# <span data-ttu-id="240d9-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="240d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="240d9-102">SYNOPSIS</span></span>
<span data-ttu-id="240d9-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="240d9-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="240d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="240d9-104">SYNTAX</span></span>

### <span data-ttu-id="240d9-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="240d9-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240d9-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="240d9-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240d9-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="240d9-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240d9-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="240d9-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="240d9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="240d9-109">DESCRIPTION</span></span>
<span data-ttu-id="240d9-110">Az **Újraindítás – AzureRmVM** parancsmag újraindítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="240d9-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="240d9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="240d9-111">EXAMPLES</span></span>

### <span data-ttu-id="240d9-112">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="240d9-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="240d9-113">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="240d9-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="240d9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="240d9-114">PARAMETERS</span></span>

### <span data-ttu-id="240d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240d9-115">-DefaultProfile</span></span>
<span data-ttu-id="240d9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="240d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240d9-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="240d9-117">-Id</span></span>
<span data-ttu-id="240d9-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="240d9-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240d9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="240d9-119">-Name</span></span>
<span data-ttu-id="240d9-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="240d9-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240d9-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="240d9-121">-PerformMaintenance</span></span>
<span data-ttu-id="240d9-122">A virtuális gép karbantartásának elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="240d9-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="240d9-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="240d9-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240d9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="240d9-125">-Confirm</span></span>
<span data-ttu-id="240d9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="240d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240d9-127">-WhatIf</span></span>
<span data-ttu-id="240d9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="240d9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="240d9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="240d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="240d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240d9-130">CommonParameters</span></span>
<span data-ttu-id="240d9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="240d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240d9-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240d9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240d9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="240d9-133">INPUTS</span></span>

## <span data-ttu-id="240d9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="240d9-134">OUTPUTS</span></span>

## <span data-ttu-id="240d9-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="240d9-135">NOTES</span></span>

## <span data-ttu-id="240d9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="240d9-136">RELATED LINKS</span></span>

[<span data-ttu-id="240d9-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="240d9-138">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="240d9-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="240d9-140">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="240d9-141">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="240d9-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="240d9-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


