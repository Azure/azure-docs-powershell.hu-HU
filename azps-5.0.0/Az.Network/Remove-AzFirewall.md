---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195347"
---
# <span data-ttu-id="4c5c7-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c5c7-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="4c5c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5c7-103">Távolítson el egy tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-103">Remove a Firewall.</span></span>

## <span data-ttu-id="4c5c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c5c7-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c5c7-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5c7-106">A **Remove-AzFirewall** parancsmag eltávolítja az Azure-tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="4c5c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c5c7-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5c7-108">Példa 1: tűzfal létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="4c5c7-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4c5c7-109">Ez a példa létrehoz egy tűzfalat, majd törli azt.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="4c5c7-110">Ha el szeretné tiltani a tűzfal törlésére vonatkozó kérdést, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="4c5c7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c5c7-111">PARAMETERS</span></span>

### <span data-ttu-id="4c5c7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c5c7-112">-AsJob</span></span>
<span data-ttu-id="4c5c7-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4c5c7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c5c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5c7-114">-DefaultProfile</span></span>
<span data-ttu-id="4c5c7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c5c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4c5c7-116">-Force</span></span>
<span data-ttu-id="4c5c7-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c5c7-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c5c7-118">-Name</span></span>
<span data-ttu-id="4c5c7-119">Annak a tűzfalnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c5c7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c5c7-120">-PassThru</span></span>
<span data-ttu-id="4c5c7-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4c5c7-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4c5c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c5c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c5c7-124">Annak a csoportnak a neve, amely a parancsmag által eltávolított tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c5c7-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c5c7-125">-Confirm</span></span>
<span data-ttu-id="4c5c7-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c5c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5c7-127">-WhatIf</span></span>
<span data-ttu-id="4c5c7-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c5c7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c5c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c5c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5c7-130">CommonParameters</span></span>
<span data-ttu-id="4c5c7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c5c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5c7-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c5c7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5c7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c5c7-133">INPUTS</span></span>

### <span data-ttu-id="4c5c7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4c5c7-134">System.String</span></span>

## <span data-ttu-id="4c5c7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c5c7-135">OUTPUTS</span></span>

### <span data-ttu-id="4c5c7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c5c7-136">System.Boolean</span></span>

## <span data-ttu-id="4c5c7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c5c7-137">NOTES</span></span>

## <span data-ttu-id="4c5c7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c5c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c5c7-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c5c7-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="4c5c7-140">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c5c7-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4c5c7-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c5c7-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
