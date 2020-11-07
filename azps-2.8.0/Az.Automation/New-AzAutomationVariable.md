---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: ea07e0d0b0c60b35186224d7ea0284df17d1e27b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667783"
---
# <span data-ttu-id="3565d-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3565d-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="3565d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3565d-102">SYNOPSIS</span></span>
<span data-ttu-id="3565d-103">Automatizálási változót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3565d-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="3565d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3565d-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3565d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3565d-105">DESCRIPTION</span></span>
<span data-ttu-id="3565d-106">A **New-AzAutomationVariable** parancsmag egy változót hoz létre az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="3565d-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="3565d-107">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3565d-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="3565d-108">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="3565d-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="3565d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3565d-109">EXAMPLES</span></span>

### <span data-ttu-id="3565d-110">Példa 1: változó létrehozása egyszerű értékkel</span><span class="sxs-lookup"><span data-stu-id="3565d-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3565d-111">Ez a parancs létrehoz egy StringVariable22 nevű változót, amelynek karakterlánc értéke a Contoso17 nevű automatizálási fiókban van.</span><span class="sxs-lookup"><span data-stu-id="3565d-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3565d-112">2. példa: változó létrehozása komplex értékkel</span><span class="sxs-lookup"><span data-stu-id="3565d-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3565d-113">Az első parancs a virtuális gépet az Get-AzVM parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3565d-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3565d-114">A parancs a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3565d-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3565d-115">A második parancs egy ComplexVariable01 nevű változót hoz létre a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="3565d-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3565d-116">Ez a parancs egy komplex objektumot használ az értékéhez, ebben az esetben a virtuális gép $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3565d-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="3565d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3565d-117">PARAMETERS</span></span>

### <span data-ttu-id="3565d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3565d-118">-AutomationAccountName</span></span>
<span data-ttu-id="3565d-119">Annak az automatizálási fióknak a nevét adja meg, amelybe a változót menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="3565d-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="3565d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3565d-120">-DefaultProfile</span></span>
<span data-ttu-id="3565d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3565d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3565d-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3565d-122">-Description</span></span>
<span data-ttu-id="3565d-123">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3565d-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="3565d-124">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="3565d-124">-Encrypted</span></span>
<span data-ttu-id="3565d-125">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="3565d-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3565d-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3565d-126">-Name</span></span>
<span data-ttu-id="3565d-127">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3565d-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="3565d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3565d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3565d-129">Azt az erőforráscsoport-csoportot adja meg, amelyhez a parancsmag létrehoz egy változót.</span><span class="sxs-lookup"><span data-stu-id="3565d-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="3565d-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="3565d-130">-Value</span></span>
<span data-ttu-id="3565d-131">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3565d-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3565d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3565d-132">CommonParameters</span></span>
<span data-ttu-id="3565d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3565d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3565d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3565d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3565d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3565d-135">INPUTS</span></span>

### <span data-ttu-id="3565d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3565d-136">System.String</span></span>

### <span data-ttu-id="3565d-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3565d-137">System.Boolean</span></span>

### <span data-ttu-id="3565d-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3565d-138">System.Object</span></span>

## <span data-ttu-id="3565d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3565d-139">OUTPUTS</span></span>

### <span data-ttu-id="3565d-140">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="3565d-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="3565d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3565d-141">NOTES</span></span>

## <span data-ttu-id="3565d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3565d-142">RELATED LINKS</span></span>

[<span data-ttu-id="3565d-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3565d-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="3565d-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3565d-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="3565d-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3565d-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


