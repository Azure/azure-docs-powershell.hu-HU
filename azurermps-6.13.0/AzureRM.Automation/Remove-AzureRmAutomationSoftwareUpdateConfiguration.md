---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494191"
---
# <span data-ttu-id="a86f4-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f4-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a86f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a86f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a86f4-103">Az Azure automatizálási szoftverfrissítés konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a86f4-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a86f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a86f4-104">SYNTAX</span></span>

### <span data-ttu-id="a86f4-105">BySucName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a86f4-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a86f4-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="a86f4-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86f4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a86f4-107">DESCRIPTION</span></span>
<span data-ttu-id="a86f4-108">Ez a parancsmag eltávolított egy Azure automatizálási szoftverfrissítési konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a86f4-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="a86f4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a86f4-109">EXAMPLES</span></span>

### <span data-ttu-id="a86f4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a86f4-110">Example 1</span></span>
<span data-ttu-id="a86f4-111">Ez a példa bemutatja, hogyan távolíthatja el a "MyUpdateConfiguration" az automatizálási fiókból</span><span class="sxs-lookup"><span data-stu-id="a86f4-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="a86f4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a86f4-112">PARAMETERS</span></span>

### <span data-ttu-id="a86f4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a86f4-113">-AutomationAccountName</span></span>
<span data-ttu-id="a86f4-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a86f4-114">The automation account name.</span></span>

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

### <span data-ttu-id="a86f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86f4-115">-DefaultProfile</span></span>
<span data-ttu-id="a86f4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a86f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a86f4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a86f4-117">-Name</span></span>
<span data-ttu-id="a86f4-118">Az eltávolítandó szoftverfrissítési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="a86f4-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86f4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a86f4-119">-PassThru</span></span>
<span data-ttu-id="a86f4-120">A PassThru egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a86f4-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a86f4-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a86f4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a86f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="a86f4-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a86f4-123">The resource group name.</span></span>

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

### <span data-ttu-id="a86f4-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f4-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="a86f4-125">Az eltávolítandó szoftverfrissítési konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="a86f4-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86f4-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a86f4-126">-Confirm</span></span>
<span data-ttu-id="a86f4-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a86f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86f4-128">-WhatIf</span></span>
<span data-ttu-id="a86f4-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a86f4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86f4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a86f4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86f4-131">CommonParameters</span></span>
<span data-ttu-id="a86f4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a86f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86f4-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86f4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86f4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86f4-134">INPUTS</span></span>

### <span data-ttu-id="a86f4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a86f4-135">System.String</span></span>

### <span data-ttu-id="a86f4-136">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f4-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a86f4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86f4-137">OUTPUTS</span></span>

### <span data-ttu-id="a86f4-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a86f4-138">System.Object</span></span>
## <span data-ttu-id="a86f4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a86f4-139">NOTES</span></span>

## <span data-ttu-id="a86f4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a86f4-140">RELATED LINKS</span></span>
