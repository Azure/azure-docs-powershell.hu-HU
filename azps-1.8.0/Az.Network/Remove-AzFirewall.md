---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670166"
---
# <span data-ttu-id="a0b8d-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a0b8d-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="a0b8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b8d-103">Távolítson el egy tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-103">Remove a Firewall.</span></span>

## <span data-ttu-id="a0b8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0b8d-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b8d-106">A **Remove-AzFirewall** parancsmag eltávolítja az Azure-tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="a0b8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0b8d-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b8d-108">1: tűzfal létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="a0b8d-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a0b8d-109">Ez a példa létrehoz egy tűzfalat, majd törli azt.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="a0b8d-110">Ha el szeretné tiltani a tűzfal törlésére vonatkozó kérdést, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="a0b8d-111">2: a tűzfal defoglalása, majd a tűzfal törlése</span><span class="sxs-lookup"><span data-stu-id="a0b8d-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a0b8d-112">Ez a példa beolvassa a tűzfalat, felszabadítja a tűzfalat, majd törli a tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="a0b8d-113">A kifoglalás parancs eltávolítja a futó szolgáltatást, de megőrzi a tűzfal konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="a0b8d-114">Ha a felhasználó ismét el szeretné indítani a szolgáltatást, a kiosztási módszert a tűzfalon kell megneveznie.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="a0b8d-115">Ha el szeretné tiltani a tűzfal törlésére vonatkozó kérdést, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="a0b8d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0b8d-116">PARAMETERS</span></span>

### <span data-ttu-id="a0b8d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0b8d-117">-AsJob</span></span>
<span data-ttu-id="a0b8d-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a0b8d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0b8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b8d-119">-DefaultProfile</span></span>
<span data-ttu-id="a0b8d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0b8d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a0b8d-121">-Force</span></span>
<span data-ttu-id="a0b8d-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0b8d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0b8d-123">-Name</span></span>
<span data-ttu-id="a0b8d-124">Annak a tűzfalnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0b8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0b8d-125">-PassThru</span></span>
<span data-ttu-id="a0b8d-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0b8d-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0b8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0b8d-129">Annak a csoportnak a neve, amely a parancsmag által eltávolított tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0b8d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0b8d-130">-Confirm</span></span>
<span data-ttu-id="a0b8d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0b8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b8d-132">-WhatIf</span></span>
<span data-ttu-id="a0b8d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0b8d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0b8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b8d-135">CommonParameters</span></span>
<span data-ttu-id="a0b8d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0b8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b8d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b8d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b8d-138">INPUTS</span></span>

### <span data-ttu-id="a0b8d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b8d-139">System.String</span></span>

## <span data-ttu-id="a0b8d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b8d-140">OUTPUTS</span></span>

### <span data-ttu-id="a0b8d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0b8d-141">System.Boolean</span></span>

## <span data-ttu-id="a0b8d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0b8d-142">NOTES</span></span>

## <span data-ttu-id="a0b8d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0b8d-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0b8d-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a0b8d-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="a0b8d-145">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a0b8d-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a0b8d-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a0b8d-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
