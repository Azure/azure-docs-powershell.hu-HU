---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493571"
---
# <span data-ttu-id="306b4-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="306b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="306b4-102">SYNOPSIS</span></span>
<span data-ttu-id="306b4-103">Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="306b4-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="306b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="306b4-104">SYNTAX</span></span>

### <span data-ttu-id="306b4-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="306b4-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306b4-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="306b4-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="306b4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="306b4-107">DESCRIPTION</span></span>
<span data-ttu-id="306b4-108">A **Start-AzureRmVM** parancsmag egy Azure virtuális gépet indít el.</span><span class="sxs-lookup"><span data-stu-id="306b4-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="306b4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="306b4-109">EXAMPLES</span></span>

### <span data-ttu-id="306b4-110">Példa 1: virtuális gép indítása</span><span class="sxs-lookup"><span data-stu-id="306b4-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="306b4-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="306b4-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="306b4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="306b4-112">PARAMETERS</span></span>

### <span data-ttu-id="306b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306b4-113">-DefaultProfile</span></span>
<span data-ttu-id="306b4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="306b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="306b4-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="306b4-115">-Id</span></span>
<span data-ttu-id="306b4-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="306b4-116">The resource group name.</span></span>

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

### <span data-ttu-id="306b4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="306b4-117">-Name</span></span>
<span data-ttu-id="306b4-118">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="306b4-118">The virtual machine name.</span></span>

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

### <span data-ttu-id="306b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="306b4-120">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="306b4-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="306b4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="306b4-121">-Confirm</span></span>
<span data-ttu-id="306b4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="306b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306b4-123">-WhatIf</span></span>
<span data-ttu-id="306b4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="306b4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="306b4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="306b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306b4-126">CommonParameters</span></span>
<span data-ttu-id="306b4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="306b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306b4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="306b4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306b4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="306b4-129">INPUTS</span></span>

## <span data-ttu-id="306b4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="306b4-130">OUTPUTS</span></span>

## <span data-ttu-id="306b4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="306b4-131">NOTES</span></span>

## <span data-ttu-id="306b4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="306b4-132">RELATED LINKS</span></span>

[<span data-ttu-id="306b4-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="306b4-134">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="306b4-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="306b4-136">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="306b4-137">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="306b4-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="306b4-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


