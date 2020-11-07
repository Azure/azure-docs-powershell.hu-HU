---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847349"
---
# <span data-ttu-id="43e6f-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="43e6f-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="43e6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="43e6f-103">Automatizálási változó módosítása</span><span class="sxs-lookup"><span data-stu-id="43e6f-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="43e6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43e6f-104">SYNTAX</span></span>

### <span data-ttu-id="43e6f-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="43e6f-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43e6f-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="43e6f-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43e6f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43e6f-107">DESCRIPTION</span></span>
<span data-ttu-id="43e6f-108">A **set-AzAutomationVariable** parancsmag módosítja az Azure automatizálási változók értékét vagy leírását.</span><span class="sxs-lookup"><span data-stu-id="43e6f-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="43e6f-109">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="43e6f-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="43e6f-110">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="43e6f-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="43e6f-111">A meglévő, nem titkosított, változókkal való *titkosítás* megadása sikertelen.</span><span class="sxs-lookup"><span data-stu-id="43e6f-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="43e6f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="43e6f-112">EXAMPLES</span></span>

### <span data-ttu-id="43e6f-113">Példa 1: változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="43e6f-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="43e6f-114">Ez a parancs a StringVariable22 nevű változó új értékét állítja be a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="43e6f-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="43e6f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43e6f-115">PARAMETERS</span></span>

### <span data-ttu-id="43e6f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43e6f-116">-AutomationAccountName</span></span>
<span data-ttu-id="43e6f-117">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolják.</span><span class="sxs-lookup"><span data-stu-id="43e6f-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="43e6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e6f-118">-DefaultProfile</span></span>
<span data-ttu-id="43e6f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43e6f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43e6f-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="43e6f-120">-Description</span></span>
<span data-ttu-id="43e6f-121">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="43e6f-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="43e6f-122">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="43e6f-122">-Encrypted</span></span>
<span data-ttu-id="43e6f-123">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="43e6f-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="43e6f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43e6f-124">-Name</span></span>
<span data-ttu-id="43e6f-125">A parancsmag által módosított változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43e6f-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="43e6f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e6f-126">-ResourceGroupName</span></span>
<span data-ttu-id="43e6f-127">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag módosított egy változót.</span><span class="sxs-lookup"><span data-stu-id="43e6f-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="43e6f-128">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="43e6f-128">-Value</span></span>
<span data-ttu-id="43e6f-129">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43e6f-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="43e6f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e6f-130">CommonParameters</span></span>
<span data-ttu-id="43e6f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43e6f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e6f-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43e6f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e6f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43e6f-133">INPUTS</span></span>

### <span data-ttu-id="43e6f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="43e6f-134">System.String</span></span>

### <span data-ttu-id="43e6f-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43e6f-135">System.Boolean</span></span>

### <span data-ttu-id="43e6f-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="43e6f-136">System.Object</span></span>

## <span data-ttu-id="43e6f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43e6f-137">OUTPUTS</span></span>

### <span data-ttu-id="43e6f-138">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="43e6f-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="43e6f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43e6f-139">NOTES</span></span>

## <span data-ttu-id="43e6f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43e6f-140">RELATED LINKS</span></span>

[<span data-ttu-id="43e6f-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="43e6f-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="43e6f-142">Új – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="43e6f-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="43e6f-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="43e6f-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

