---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: df38df4da3fada0e89f527e7655c5c62c0df2602
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492553"
---
# <span data-ttu-id="59d33-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="59d33-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="59d33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59d33-102">SYNOPSIS</span></span>
<span data-ttu-id="59d33-103">Eltávolítja a séf kiterjesztését egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="59d33-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59d33-104">SYNTAX</span></span>

### <span data-ttu-id="59d33-105">Linux</span><span class="sxs-lookup"><span data-stu-id="59d33-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d33-106">Windows</span><span class="sxs-lookup"><span data-stu-id="59d33-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d33-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="59d33-107">DESCRIPTION</span></span>
<span data-ttu-id="59d33-108">A **Remove-AzureVMChefExtension** parancsmag eltávolítja a Chef bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="59d33-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="59d33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59d33-109">EXAMPLES</span></span>

### <span data-ttu-id="59d33-110">Példa 1: Chef-kiterjesztés eltávolítása Windows Virtual Machine-ből</span><span class="sxs-lookup"><span data-stu-id="59d33-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="59d33-111">Ez a parancs eltávolítja a Chef bővítményt egy, a WindowsVM001 nevű Windows-beli virtuális gépről, amely a ResourceGroup001 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="59d33-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="59d33-112">2. példa: Chef-kiterjesztés eltávolítása egy linuxos virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="59d33-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="59d33-113">Ez a parancs eltávolítja a Chef bővítményt egy LinuxVM001 nevű, a ResourceGroup002 nevű erőforráscsoport csoportjába tartozó Linux-beli virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="59d33-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="59d33-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59d33-114">PARAMETERS</span></span>

### <span data-ttu-id="59d33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d33-115">-DefaultProfile</span></span>
<span data-ttu-id="59d33-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59d33-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d33-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="59d33-117">-Linux</span></span>
<span data-ttu-id="59d33-118">Azt jelzi, hogy ez a parancsmag egy linuxos virtuális gépet céloz meg.</span><span class="sxs-lookup"><span data-stu-id="59d33-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d33-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59d33-119">-Name</span></span>
<span data-ttu-id="59d33-120">Annak a séf-bővítménynek a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="59d33-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d33-121">-ResourceGroupName</span></span>
<span data-ttu-id="59d33-122">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59d33-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d33-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="59d33-123">-VMName</span></span>
<span data-ttu-id="59d33-124">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a szakács bővítményt.</span><span class="sxs-lookup"><span data-stu-id="59d33-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d33-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="59d33-125">-Windows</span></span>
<span data-ttu-id="59d33-126">Jelzi, hogy ez a parancsmag a Windows Virtual Machine-t célozza meg.</span><span class="sxs-lookup"><span data-stu-id="59d33-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d33-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59d33-127">-Confirm</span></span>
<span data-ttu-id="59d33-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59d33-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d33-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d33-129">-WhatIf</span></span>
<span data-ttu-id="59d33-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59d33-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="59d33-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59d33-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d33-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d33-132">CommonParameters</span></span>
<span data-ttu-id="59d33-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59d33-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d33-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d33-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d33-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d33-135">INPUTS</span></span>

## <span data-ttu-id="59d33-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d33-136">OUTPUTS</span></span>

## <span data-ttu-id="59d33-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59d33-137">NOTES</span></span>

## <span data-ttu-id="59d33-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59d33-138">RELATED LINKS</span></span>

[<span data-ttu-id="59d33-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="59d33-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="59d33-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="59d33-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
