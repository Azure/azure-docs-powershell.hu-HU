---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940177"
---
# <span data-ttu-id="96411-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96411-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="96411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96411-102">SYNOPSIS</span></span>
<span data-ttu-id="96411-103">Tűzfal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="96411-103">Remove a Firewall.</span></span>

## <span data-ttu-id="96411-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96411-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96411-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96411-105">DESCRIPTION</span></span>
<span data-ttu-id="96411-106">A **Remove-AzFirewall** parancsmag eltávolítja az Azure tűzfalat.</span><span class="sxs-lookup"><span data-stu-id="96411-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="96411-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96411-107">EXAMPLES</span></span>

### <span data-ttu-id="96411-108">1. példa: Tűzfal létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="96411-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="96411-109">Ez a példa létrehoz egy tűzfalat, majd törli azt.</span><span class="sxs-lookup"><span data-stu-id="96411-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="96411-110">A tűzfal törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="96411-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="96411-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96411-111">PARAMETERS</span></span>

### <span data-ttu-id="96411-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96411-112">-AsJob</span></span>
<span data-ttu-id="96411-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="96411-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96411-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96411-114">-DefaultProfile</span></span>
<span data-ttu-id="96411-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96411-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96411-116">-Force</span><span class="sxs-lookup"><span data-stu-id="96411-116">-Force</span></span>
<span data-ttu-id="96411-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="96411-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96411-118">-Name</span><span class="sxs-lookup"><span data-stu-id="96411-118">-Name</span></span>
<span data-ttu-id="96411-119">Annak a tűzfalnak a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96411-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96411-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96411-120">-PassThru</span></span>
<span data-ttu-id="96411-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="96411-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96411-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="96411-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96411-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96411-123">-ResourceGroupName</span></span>
<span data-ttu-id="96411-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="96411-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96411-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96411-125">-Confirm</span></span>
<span data-ttu-id="96411-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96411-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96411-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96411-127">-WhatIf</span></span>
<span data-ttu-id="96411-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96411-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96411-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96411-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96411-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96411-130">CommonParameters</span></span>
<span data-ttu-id="96411-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96411-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96411-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96411-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96411-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96411-133">INPUTS</span></span>

### <span data-ttu-id="96411-134">System.String</span><span class="sxs-lookup"><span data-stu-id="96411-134">System.String</span></span>

## <span data-ttu-id="96411-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96411-135">OUTPUTS</span></span>

### <span data-ttu-id="96411-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96411-136">System.Boolean</span></span>

## <span data-ttu-id="96411-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96411-137">NOTES</span></span>

## <span data-ttu-id="96411-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96411-138">RELATED LINKS</span></span>

[<span data-ttu-id="96411-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96411-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="96411-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96411-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="96411-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96411-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
