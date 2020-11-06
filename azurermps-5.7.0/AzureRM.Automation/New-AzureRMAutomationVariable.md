---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503103"
---
# <span data-ttu-id="0ad15-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0ad15-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="0ad15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ad15-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad15-103">Automatizálási változót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0ad15-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ad15-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad15-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ad15-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad15-106">A **New-AzureRmAutomationVariable** parancsmag egy változót hoz létre az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="0ad15-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="0ad15-107">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ad15-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="0ad15-108">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="0ad15-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="0ad15-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ad15-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad15-110">Példa 1: változó létrehozása egyszerű értékkel</span><span class="sxs-lookup"><span data-stu-id="0ad15-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0ad15-111">Ez a parancs létrehoz egy StringVariable22 nevű változót, amelynek karakterlánc értéke a Contoso17 nevű automatizálási fiókban van.</span><span class="sxs-lookup"><span data-stu-id="0ad15-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0ad15-112">2. példa: változó létrehozása komplex értékkel</span><span class="sxs-lookup"><span data-stu-id="0ad15-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0ad15-113">Az első parancs a virtuális gépet az Get-AzureVM parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad15-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="0ad15-114">A parancs a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0ad15-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="0ad15-115">A második parancs egy ComplexVariable01 nevű változót hoz létre a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="0ad15-116">Ez a parancs egy komplex objektumot használ az értékéhez, ebben az esetben a virtuális gép $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="0ad15-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">PARAMETERS</span></span>

### <span data-ttu-id="0ad15-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">-AutomationAccountName</span></span>
<span data-ttu-id="0ad15-119">Annak az automatizálási fióknak a nevét adja meg, amelybe a változót menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">Specifies the name of the Automation account in which to store the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">-DefaultProfile</span></span>
<span data-ttu-id="0ad15-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">-Description</span></span>
<span data-ttu-id="0ad15-123">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-124">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="0ad15-124">-Encrypted</span></span>
<span data-ttu-id="0ad15-125">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">-Name</span></span>
<span data-ttu-id="0ad15-127">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad15-127">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad15-128">-ResourceGroupName</span></span>
<span data-ttu-id="0ad15-129">Azt az erőforráscsoport-csoportot adja meg, amelyhez a parancsmag létrehoz egy változót.</span><span class="sxs-lookup"><span data-stu-id="0ad15-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="0ad15-130">-Value</span></span>
<span data-ttu-id="0ad15-131">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad15-131">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad15-132">CommonParameters</span></span>
<span data-ttu-id="0ad15-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ad15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad15-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad15-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad15-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad15-135">INPUTS</span></span>

### <span data-ttu-id="0ad15-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ad15-136">None</span></span>
<span data-ttu-id="0ad15-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0ad15-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ad15-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad15-138">OUTPUTS</span></span>

### <span data-ttu-id="0ad15-139">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="0ad15-139">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0ad15-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ad15-140">NOTES</span></span>

## <span data-ttu-id="0ad15-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ad15-141">RELATED LINKS</span></span>

[<span data-ttu-id="0ad15-142">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0ad15-142">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="0ad15-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0ad15-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="0ad15-144">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0ad15-144">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)

