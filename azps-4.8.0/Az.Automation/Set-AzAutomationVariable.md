---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024213"
---
# <span data-ttu-id="868ec-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="868ec-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="868ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="868ec-102">SYNOPSIS</span></span>
<span data-ttu-id="868ec-103">Automatizálási változó módosítása</span><span class="sxs-lookup"><span data-stu-id="868ec-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="868ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="868ec-104">SYNTAX</span></span>

### <span data-ttu-id="868ec-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="868ec-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="868ec-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="868ec-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="868ec-107">DESCRIPTION</span></span>
<span data-ttu-id="868ec-108">A **set-AzAutomationVariable** parancsmag módosítja az Azure automatizálási változók értékét vagy leírását.</span><span class="sxs-lookup"><span data-stu-id="868ec-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="868ec-109">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="868ec-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="868ec-110">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="868ec-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="868ec-111">A meglévő, nem titkosított, változókkal való *titkosítás* megadása sikertelen.</span><span class="sxs-lookup"><span data-stu-id="868ec-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="868ec-112">Példák</span><span class="sxs-lookup"><span data-stu-id="868ec-112">EXAMPLES</span></span>

### <span data-ttu-id="868ec-113">Példa 1: változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="868ec-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="868ec-114">Ez a parancs a StringVariable22 nevű változó új értékét állítja be a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="868ec-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="868ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="868ec-115">PARAMETERS</span></span>

### <span data-ttu-id="868ec-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="868ec-116">-AutomationAccountName</span></span>
<span data-ttu-id="868ec-117">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolják.</span><span class="sxs-lookup"><span data-stu-id="868ec-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="868ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868ec-118">-DefaultProfile</span></span>
<span data-ttu-id="868ec-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="868ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="868ec-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="868ec-120">-Description</span></span>
<span data-ttu-id="868ec-121">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ec-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="868ec-122">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="868ec-122">-Encrypted</span></span>
<span data-ttu-id="868ec-123">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="868ec-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="868ec-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="868ec-124">-Name</span></span>
<span data-ttu-id="868ec-125">A parancsmag által módosított változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ec-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="868ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="868ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="868ec-127">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag módosított egy változót.</span><span class="sxs-lookup"><span data-stu-id="868ec-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="868ec-128">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="868ec-128">-Value</span></span>
<span data-ttu-id="868ec-129">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="868ec-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="868ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868ec-130">CommonParameters</span></span>
<span data-ttu-id="868ec-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="868ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868ec-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="868ec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868ec-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="868ec-133">INPUTS</span></span>

### <span data-ttu-id="868ec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="868ec-134">System.String</span></span>

### <span data-ttu-id="868ec-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="868ec-135">System.Boolean</span></span>

### <span data-ttu-id="868ec-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="868ec-136">System.Object</span></span>

## <span data-ttu-id="868ec-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="868ec-137">OUTPUTS</span></span>

### <span data-ttu-id="868ec-138">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="868ec-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="868ec-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="868ec-139">NOTES</span></span>

## <span data-ttu-id="868ec-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="868ec-140">RELATED LINKS</span></span>

[<span data-ttu-id="868ec-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="868ec-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="868ec-142">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="868ec-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="868ec-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="868ec-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


