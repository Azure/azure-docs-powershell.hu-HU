---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373027"
---
# <span data-ttu-id="b11db-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b11db-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="b11db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11db-102">SYNOPSIS</span></span>
<span data-ttu-id="b11db-103">Módosít egy Automatizálási változót.</span><span class="sxs-lookup"><span data-stu-id="b11db-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="b11db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b11db-104">SYNTAX</span></span>

### <span data-ttu-id="b11db-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="b11db-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b11db-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="b11db-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b11db-107">DESCRIPTION</span></span>
<span data-ttu-id="b11db-108">A **Set-AzAutomationVariable** parancsmag módosítja egy azure-automatizálási változó értékét vagy leírását.</span><span class="sxs-lookup"><span data-stu-id="b11db-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="b11db-109">A változó titkosításához adja meg *a Titkosított paramétert.*</span><span class="sxs-lookup"><span data-stu-id="b11db-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b11db-110">Létrehozás után a változó titkosított állapota nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="b11db-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="b11db-111">A Titkosított *érték megadása* egy meglévő, nem titkosított változó esetén sikertelen.</span><span class="sxs-lookup"><span data-stu-id="b11db-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="b11db-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b11db-112">EXAMPLES</span></span>

### <span data-ttu-id="b11db-113">1. példa: Változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="b11db-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="b11db-114">Ez a parancs beállítja a Contoso17 nevű Azure Automation-fiók KarakterláncVáltozó22 nevű változóját.</span><span class="sxs-lookup"><span data-stu-id="b11db-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b11db-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b11db-115">PARAMETERS</span></span>

### <span data-ttu-id="b11db-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b11db-116">-AutomationAccountName</span></span>
<span data-ttu-id="b11db-117">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolja.</span><span class="sxs-lookup"><span data-stu-id="b11db-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="b11db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11db-118">-DefaultProfile</span></span>
<span data-ttu-id="b11db-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b11db-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b11db-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b11db-120">-Description</span></span>
<span data-ttu-id="b11db-121">Megadja a változó leírását.</span><span class="sxs-lookup"><span data-stu-id="b11db-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-122">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="b11db-122">-Encrypted</span></span>
<span data-ttu-id="b11db-123">Azt adja meg, hogy a parancsmag titkosítsa-e a tároló változó értékét.</span><span class="sxs-lookup"><span data-stu-id="b11db-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b11db-124">-Name</span></span>
<span data-ttu-id="b11db-125">Annak a változónak a nevét adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="b11db-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b11db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11db-126">-ResourceGroupName</span></span>
<span data-ttu-id="b11db-127">Azt az erőforráscsoportot adja meg, amelynek a parancsmagja módosít egy változót.</span><span class="sxs-lookup"><span data-stu-id="b11db-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="b11db-128">-Érték</span><span class="sxs-lookup"><span data-stu-id="b11db-128">-Value</span></span>
<span data-ttu-id="b11db-129">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b11db-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11db-130">CommonParameters</span></span>
<span data-ttu-id="b11db-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11db-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11db-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11db-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b11db-133">INPUTS</span></span>

### <span data-ttu-id="b11db-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b11db-134">System.String</span></span>

### <span data-ttu-id="b11db-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b11db-135">System.Boolean</span></span>

### <span data-ttu-id="b11db-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="b11db-136">System.Object</span></span>

## <span data-ttu-id="b11db-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b11db-137">OUTPUTS</span></span>

### <span data-ttu-id="b11db-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="b11db-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b11db-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b11db-139">NOTES</span></span>

## <span data-ttu-id="b11db-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b11db-140">RELATED LINKS</span></span>

[<span data-ttu-id="b11db-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b11db-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="b11db-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b11db-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="b11db-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b11db-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


