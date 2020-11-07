---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: bc0fb96ace958761f4d6b12b73ac46b93d9a0143
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671495"
---
# <span data-ttu-id="59a94-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="59a94-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="59a94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59a94-102">SYNOPSIS</span></span>
<span data-ttu-id="59a94-103">Automatizálási változó módosítása</span><span class="sxs-lookup"><span data-stu-id="59a94-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="59a94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59a94-104">SYNTAX</span></span>

### <span data-ttu-id="59a94-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="59a94-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59a94-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="59a94-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59a94-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="59a94-107">DESCRIPTION</span></span>
<span data-ttu-id="59a94-108">A **set-AzAutomationVariable** parancsmag módosítja az Azure automatizálási változók értékét vagy leírását.</span><span class="sxs-lookup"><span data-stu-id="59a94-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="59a94-109">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="59a94-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="59a94-110">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="59a94-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="59a94-111">A meglévő, nem titkosított, változókkal való *titkosítás* megadása sikertelen.</span><span class="sxs-lookup"><span data-stu-id="59a94-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="59a94-112">Példák</span><span class="sxs-lookup"><span data-stu-id="59a94-112">EXAMPLES</span></span>

### <span data-ttu-id="59a94-113">Példa 1: változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="59a94-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="59a94-114">Ez a parancs a StringVariable22 nevű változó új értékét állítja be a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="59a94-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="59a94-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59a94-115">PARAMETERS</span></span>

### <span data-ttu-id="59a94-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59a94-116">-AutomationAccountName</span></span>
<span data-ttu-id="59a94-117">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolják.</span><span class="sxs-lookup"><span data-stu-id="59a94-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="59a94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a94-118">-DefaultProfile</span></span>
<span data-ttu-id="59a94-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59a94-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a94-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="59a94-120">-Description</span></span>
<span data-ttu-id="59a94-121">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="59a94-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="59a94-122">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="59a94-122">-Encrypted</span></span>
<span data-ttu-id="59a94-123">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="59a94-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="59a94-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59a94-124">-Name</span></span>
<span data-ttu-id="59a94-125">A parancsmag által módosított változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59a94-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="59a94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a94-126">-ResourceGroupName</span></span>
<span data-ttu-id="59a94-127">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag módosított egy változót.</span><span class="sxs-lookup"><span data-stu-id="59a94-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="59a94-128">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="59a94-128">-Value</span></span>
<span data-ttu-id="59a94-129">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59a94-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="59a94-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a94-130">CommonParameters</span></span>
<span data-ttu-id="59a94-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59a94-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a94-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a94-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a94-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a94-133">INPUTS</span></span>

### <span data-ttu-id="59a94-134">System. String</span><span class="sxs-lookup"><span data-stu-id="59a94-134">System.String</span></span>

### <span data-ttu-id="59a94-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59a94-135">System.Boolean</span></span>

### <span data-ttu-id="59a94-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="59a94-136">System.Object</span></span>

## <span data-ttu-id="59a94-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59a94-137">OUTPUTS</span></span>

### <span data-ttu-id="59a94-138">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="59a94-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="59a94-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59a94-139">NOTES</span></span>

## <span data-ttu-id="59a94-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59a94-140">RELATED LINKS</span></span>

[<span data-ttu-id="59a94-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="59a94-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="59a94-142">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="59a94-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="59a94-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="59a94-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


