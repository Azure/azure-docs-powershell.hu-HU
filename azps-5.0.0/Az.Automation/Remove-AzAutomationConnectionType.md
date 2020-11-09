---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299723"
---
# <span data-ttu-id="98daa-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="98daa-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="98daa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98daa-102">SYNOPSIS</span></span>
<span data-ttu-id="98daa-103">Automatizálási kapcsolat típusának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="98daa-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="98daa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98daa-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98daa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98daa-105">DESCRIPTION</span></span>
<span data-ttu-id="98daa-106">A **Remove-AzAutomationConnectionType** parancsmag kapcsolati típusát eltávolítja az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="98daa-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="98daa-107">A törölt kapcsolat típusával társított összes kapcsolat használhatatlanná válik.</span><span class="sxs-lookup"><span data-stu-id="98daa-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="98daa-108">Távolítsa el őket, hacsak nem hoz létre olyan új kapcsolattípuset, amely megfelel az alábbi követelményeknek:</span><span class="sxs-lookup"><span data-stu-id="98daa-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="98daa-109">A típus neve megegyezik az eredeti kapcsolat típusával.</span><span class="sxs-lookup"><span data-stu-id="98daa-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="98daa-110">A típus ugyanazokkal a mező-definíciókkal rendelkezik, mint az eredeti kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="98daa-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="98daa-111">További mezőket is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="98daa-111">It can have additional fields.</span></span>

## <span data-ttu-id="98daa-112">Példák</span><span class="sxs-lookup"><span data-stu-id="98daa-112">EXAMPLES</span></span>

### <span data-ttu-id="98daa-113">1. példa: kapcsolattípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98daa-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98daa-114">Ez a parancs eltávolítja a ContosoConnectionType nevű kapcsolattípus-típust a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="98daa-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="98daa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98daa-115">PARAMETERS</span></span>

### <span data-ttu-id="98daa-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98daa-116">-AutomationAccountName</span></span>
<span data-ttu-id="98daa-117">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag eltávolítja a kapcsolat típusát.</span><span class="sxs-lookup"><span data-stu-id="98daa-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="98daa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98daa-118">-DefaultProfile</span></span>
<span data-ttu-id="98daa-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98daa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98daa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="98daa-120">-Force</span></span>
<span data-ttu-id="98daa-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="98daa-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98daa-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98daa-122">-Name</span></span>
<span data-ttu-id="98daa-123">A parancsmag által eltávolított automatizálási kapcsolat típusának neve.</span><span class="sxs-lookup"><span data-stu-id="98daa-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98daa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98daa-124">-ResourceGroupName</span></span>
<span data-ttu-id="98daa-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyből ez a parancsmag eltávolítja az automatizálási kapcsolat típusát.</span><span class="sxs-lookup"><span data-stu-id="98daa-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="98daa-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98daa-126">-Confirm</span></span>
<span data-ttu-id="98daa-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98daa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98daa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98daa-128">-WhatIf</span></span>
<span data-ttu-id="98daa-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98daa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98daa-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98daa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98daa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98daa-131">CommonParameters</span></span>
<span data-ttu-id="98daa-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98daa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98daa-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98daa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98daa-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98daa-134">INPUTS</span></span>

### <span data-ttu-id="98daa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="98daa-135">System.String</span></span>

## <span data-ttu-id="98daa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98daa-136">OUTPUTS</span></span>

### <span data-ttu-id="98daa-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="98daa-137">System.Void</span></span>

## <span data-ttu-id="98daa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98daa-138">NOTES</span></span>

## <span data-ttu-id="98daa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98daa-139">RELATED LINKS</span></span>

[<span data-ttu-id="98daa-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="98daa-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


