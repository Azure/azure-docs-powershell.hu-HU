---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500876"
---
# <span data-ttu-id="8b291-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="8b291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b291-102">SYNOPSIS</span></span>
<span data-ttu-id="8b291-103">Eltávolítja a virtuális gépet az Azureról.</span><span class="sxs-lookup"><span data-stu-id="8b291-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b291-104">SYNTAX</span></span>

### <span data-ttu-id="8b291-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b291-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b291-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8b291-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b291-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b291-107">DESCRIPTION</span></span>
<span data-ttu-id="8b291-108">A **Remove-AzureRmVM** parancsmag eltávolítja a virtuális gépet az azureról.</span><span class="sxs-lookup"><span data-stu-id="8b291-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="8b291-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8b291-109">EXAMPLES</span></span>

### <span data-ttu-id="8b291-110">Példa 1: virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8b291-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8b291-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az erőforrás csoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8b291-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8b291-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b291-112">PARAMETERS</span></span>

### <span data-ttu-id="8b291-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b291-113">-DefaultProfile</span></span>
<span data-ttu-id="8b291-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b291-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b291-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b291-115">-Force</span></span>
<span data-ttu-id="8b291-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8b291-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8b291-117">-Id</span></span>
<span data-ttu-id="8b291-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8b291-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b291-119">-Name</span></span>
<span data-ttu-id="8b291-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8b291-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b291-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b291-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b291-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b291-123">-Confirm</span></span>
<span data-ttu-id="8b291-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b291-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b291-125">-WhatIf</span></span>
<span data-ttu-id="8b291-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b291-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8b291-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b291-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b291-128">CommonParameters</span></span>
<span data-ttu-id="8b291-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b291-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b291-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b291-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b291-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b291-131">INPUTS</span></span>

## <span data-ttu-id="8b291-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b291-132">OUTPUTS</span></span>

## <span data-ttu-id="8b291-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b291-133">NOTES</span></span>

## <span data-ttu-id="8b291-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b291-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b291-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8b291-136">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8b291-137">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8b291-138">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="8b291-139">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="8b291-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b291-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


