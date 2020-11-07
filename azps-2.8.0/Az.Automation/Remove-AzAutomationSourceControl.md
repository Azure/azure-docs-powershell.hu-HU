---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667757"
---
# <span data-ttu-id="b32aa-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="b32aa-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="b32aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b32aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b32aa-103">Az Azure automatizálási verziókövetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b32aa-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="b32aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b32aa-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b32aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b32aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b32aa-106">A Remove-AzAutomationSourceControl parancsmag eltávolítja a verziókövetés az Azure automatizálási szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="b32aa-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="b32aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b32aa-107">EXAMPLES</span></span>

### <span data-ttu-id="b32aa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b32aa-108">Example 1</span></span>
<span data-ttu-id="b32aa-109">Ez a parancs eltávolítja a VSTSNative nevű automatizálási forrás vezérlőt a devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="b32aa-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="b32aa-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b32aa-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="b32aa-111">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b32aa-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="b32aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b32aa-112">PARAMETERS</span></span>

### <span data-ttu-id="b32aa-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b32aa-113">-AutomationAccountName</span></span>
<span data-ttu-id="b32aa-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b32aa-114">The automation account name.</span></span>

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

### <span data-ttu-id="b32aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32aa-115">-DefaultProfile</span></span>
<span data-ttu-id="b32aa-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b32aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b32aa-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b32aa-117">-Name</span></span>
<span data-ttu-id="b32aa-118">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="b32aa-118">The source control name.</span></span>

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

### <span data-ttu-id="b32aa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b32aa-119">-PassThru</span></span>
<span data-ttu-id="b32aa-120">A PassThru egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b32aa-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b32aa-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b32aa-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="b32aa-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b32aa-123">The resource group name.</span></span>

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

### <span data-ttu-id="b32aa-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b32aa-124">-Confirm</span></span>
<span data-ttu-id="b32aa-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b32aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32aa-126">-WhatIf</span></span>
<span data-ttu-id="b32aa-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b32aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32aa-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b32aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32aa-129">CommonParameters</span></span>
<span data-ttu-id="b32aa-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b32aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32aa-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32aa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32aa-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32aa-132">INPUTS</span></span>

### <span data-ttu-id="b32aa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b32aa-133">System.String</span></span>

## <span data-ttu-id="b32aa-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32aa-134">OUTPUTS</span></span>

### <span data-ttu-id="b32aa-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="b32aa-135">System.Void</span></span>

### <span data-ttu-id="b32aa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b32aa-136">System.Boolean</span></span>

## <span data-ttu-id="b32aa-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b32aa-137">NOTES</span></span>

## <span data-ttu-id="b32aa-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b32aa-138">RELATED LINKS</span></span>
