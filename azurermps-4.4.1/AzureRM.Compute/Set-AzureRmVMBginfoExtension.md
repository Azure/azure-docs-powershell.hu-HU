---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: 4e5e4a7dda9acac6d1da9fbce7e330b8c4bbb3ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672060"
---
# <span data-ttu-id="54429-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="54429-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="54429-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54429-102">SYNOPSIS</span></span>
<span data-ttu-id="54429-103">A BGInfo bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="54429-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54429-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54429-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54429-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54429-105">DESCRIPTION</span></span>
<span data-ttu-id="54429-106">A **set-AzureRmVMBGInfoExtension** parancsmag hozzáadja a BGInfo bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="54429-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="54429-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54429-107">EXAMPLES</span></span>

### <span data-ttu-id="54429-108">Példa 1: a BGInfo bővítmény felvétele virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="54429-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="54429-109">Ez a parancs hozzáadja a BGInfo bővítményt a ContosoVM nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="54429-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="54429-110">A parancs a virtuális gép erőforrás csoportját és helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54429-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="54429-111">A parancs a bővítmény nevét és verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54429-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="54429-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54429-112">PARAMETERS</span></span>

### <span data-ttu-id="54429-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54429-113">-DefaultProfile</span></span>
<span data-ttu-id="54429-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54429-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54429-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="54429-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="54429-116">Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményt egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="54429-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="54429-117">Ez a parancsmag alapértelmezés szerint lehetővé teszi, hogy a Guest Agent frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="54429-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54429-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="54429-118">-ForceRerun</span></span>
<span data-ttu-id="54429-119">Azt adja meg, hogy a bővítményt ugyanazzal a nyilvános vagy védett beállításokkal kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="54429-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="54429-120">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="54429-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="54429-121">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="54429-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54429-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="54429-122">-Location</span></span>
<span data-ttu-id="54429-123">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54429-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54429-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54429-124">-Name</span></span>
<span data-ttu-id="54429-125">Megadja annak a BGInfo-kiterjesztésnek a nevét, amelyet a parancsmag a virtuális gépre ad.</span><span class="sxs-lookup"><span data-stu-id="54429-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54429-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54429-126">-ResourceGroupName</span></span>
<span data-ttu-id="54429-127">Annak a virtuális gépnek az erőforráscsoport nevét adja meg, amelyre a parancsmag hozzáadja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="54429-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="54429-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="54429-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="54429-129">Annak a bővítménynek a verziószámát adja meg, amelyet a parancsmag a virtuális gépre ad.</span><span class="sxs-lookup"><span data-stu-id="54429-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54429-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="54429-130">-VMName</span></span>
<span data-ttu-id="54429-131">Annak a virtuális gépnek a neve, amelyhez a parancsmag hozzáadja az BGInfo bővítményt.</span><span class="sxs-lookup"><span data-stu-id="54429-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="54429-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54429-132">-Confirm</span></span>
<span data-ttu-id="54429-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54429-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54429-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54429-134">-WhatIf</span></span>
<span data-ttu-id="54429-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54429-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="54429-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54429-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54429-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54429-137">CommonParameters</span></span>
<span data-ttu-id="54429-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54429-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54429-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54429-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54429-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54429-140">INPUTS</span></span>

## <span data-ttu-id="54429-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54429-141">OUTPUTS</span></span>

## <span data-ttu-id="54429-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54429-142">NOTES</span></span>

## <span data-ttu-id="54429-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54429-143">RELATED LINKS</span></span>

