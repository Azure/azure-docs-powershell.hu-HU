---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: d5058a3741bfaf598793f81ae030541d26aa4aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920857"
---
# <span data-ttu-id="539f8-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="539f8-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="539f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="539f8-102">SYNOPSIS</span></span>
<span data-ttu-id="539f8-103">Automatizálási változót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="539f8-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="539f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="539f8-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="539f8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="539f8-105">DESCRIPTION</span></span>
<span data-ttu-id="539f8-106">A **New-AzAutomationVariable** parancsmag létrehoz egy változót az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="539f8-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="539f8-107">A változó titkosításához adja meg *a Titkosított paramétert.*</span><span class="sxs-lookup"><span data-stu-id="539f8-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="539f8-108">Létrehozás után a változó titkosított állapota nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="539f8-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="539f8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="539f8-109">EXAMPLES</span></span>

### <span data-ttu-id="539f8-110">1. példa: Egyszerű értékkel létrehozott változó</span><span class="sxs-lookup"><span data-stu-id="539f8-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="539f8-111">Ez a parancs létrehoz egy StringVariable22 nevű változót, amely a Contoso17 nevű automatizálási fiókban egy karakterlánc-értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="539f8-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="539f8-112">2. példa: Változó létrehozása komplex értékkel</span><span class="sxs-lookup"><span data-stu-id="539f8-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="539f8-113">Az első parancs egy virtuális gépet kap a Get-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="539f8-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="539f8-114">A parancs a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="539f8-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="539f8-115">A második parancs létrehoz egy ComplexVariable01 nevű változót a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="539f8-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="539f8-116">Ez a parancs egy komplex objektumot használ az értékében, ebben az esetben a virtuális $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="539f8-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="539f8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="539f8-117">PARAMETERS</span></span>

### <span data-ttu-id="539f8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="539f8-118">-AutomationAccountName</span></span>
<span data-ttu-id="539f8-119">Annak az automatizálási fióknak a nevét adja meg, amelyben tárolni kell a változót.</span><span class="sxs-lookup"><span data-stu-id="539f8-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="539f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539f8-120">-DefaultProfile</span></span>
<span data-ttu-id="539f8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="539f8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="539f8-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="539f8-122">-Description</span></span>
<span data-ttu-id="539f8-123">Megadja a változó leírását.</span><span class="sxs-lookup"><span data-stu-id="539f8-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="539f8-124">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="539f8-124">-Encrypted</span></span>
<span data-ttu-id="539f8-125">Azt adja meg, hogy ez a parancsmag titkosítja-e a tároló változó értékét.</span><span class="sxs-lookup"><span data-stu-id="539f8-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="539f8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="539f8-126">-Name</span></span>
<span data-ttu-id="539f8-127">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="539f8-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="539f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="539f8-129">Azt az erőforráscsoportot adja meg, amelyhez a parancsmag létrehoz egy változót.</span><span class="sxs-lookup"><span data-stu-id="539f8-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="539f8-130">-Érték</span><span class="sxs-lookup"><span data-stu-id="539f8-130">-Value</span></span>
<span data-ttu-id="539f8-131">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="539f8-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="539f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539f8-132">CommonParameters</span></span>
<span data-ttu-id="539f8-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539f8-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539f8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539f8-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="539f8-135">INPUTS</span></span>

### <span data-ttu-id="539f8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="539f8-136">System.String</span></span>

### <span data-ttu-id="539f8-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="539f8-137">System.Boolean</span></span>

### <span data-ttu-id="539f8-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="539f8-138">System.Object</span></span>

## <span data-ttu-id="539f8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="539f8-139">OUTPUTS</span></span>

### <span data-ttu-id="539f8-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="539f8-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="539f8-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="539f8-141">NOTES</span></span>

## <span data-ttu-id="539f8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="539f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="539f8-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="539f8-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="539f8-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="539f8-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="539f8-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="539f8-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


