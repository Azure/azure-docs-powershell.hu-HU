---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492026"
---
# <span data-ttu-id="62232-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="62232-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="62232-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62232-102">SYNOPSIS</span></span>
<span data-ttu-id="62232-103">Automatizálási változó módosítása</span><span class="sxs-lookup"><span data-stu-id="62232-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62232-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62232-104">SYNTAX</span></span>

### <span data-ttu-id="62232-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="62232-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62232-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="62232-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62232-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62232-107">DESCRIPTION</span></span>
<span data-ttu-id="62232-108">A **set-AzureRmAutomationVariable** parancsmag módosítja az Azure automatizálási változók értékét vagy leírását.</span><span class="sxs-lookup"><span data-stu-id="62232-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="62232-109">A változó titkosításához adja meg a *titkosított* paramétert.</span><span class="sxs-lookup"><span data-stu-id="62232-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="62232-110">Létrehozása után a változók titkosított állapotát nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="62232-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="62232-111">A meglévő, nem titkosított, változókkal való *titkosítás* megadása sikertelen.</span><span class="sxs-lookup"><span data-stu-id="62232-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="62232-112">Példák</span><span class="sxs-lookup"><span data-stu-id="62232-112">EXAMPLES</span></span>

### <span data-ttu-id="62232-113">Példa 1: változó értékének beállítása</span><span class="sxs-lookup"><span data-stu-id="62232-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="62232-114">Ez a parancs a StringVariable22 nevű változó új értékét állítja be a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="62232-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="62232-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62232-115">PARAMETERS</span></span>

### <span data-ttu-id="62232-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62232-116">-AutomationAccountName</span></span>
<span data-ttu-id="62232-117">Annak az automatizálási fióknak a nevét adja meg, amelyben a változót tárolják.</span><span class="sxs-lookup"><span data-stu-id="62232-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="62232-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62232-118">-DefaultProfile</span></span>
<span data-ttu-id="62232-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62232-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62232-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="62232-120">-Description</span></span>
<span data-ttu-id="62232-121">A változó leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="62232-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="62232-122">-Titkosított</span><span class="sxs-lookup"><span data-stu-id="62232-122">-Encrypted</span></span>
<span data-ttu-id="62232-123">Meghatározza, hogy a parancsmag titkosítja-e a változó értékét a tárterület számára.</span><span class="sxs-lookup"><span data-stu-id="62232-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="62232-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62232-124">-Name</span></span>
<span data-ttu-id="62232-125">A parancsmag által módosított változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62232-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62232-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62232-126">-ResourceGroupName</span></span>
<span data-ttu-id="62232-127">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag módosított egy változót.</span><span class="sxs-lookup"><span data-stu-id="62232-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="62232-128">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="62232-128">-Value</span></span>
<span data-ttu-id="62232-129">A változó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62232-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="62232-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62232-130">CommonParameters</span></span>
<span data-ttu-id="62232-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62232-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62232-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62232-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62232-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62232-133">INPUTS</span></span>

### <span data-ttu-id="62232-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62232-134">System.String</span></span>

### <span data-ttu-id="62232-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62232-135">System.Boolean</span></span>

### <span data-ttu-id="62232-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="62232-136">System.Object</span></span>

## <span data-ttu-id="62232-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62232-137">OUTPUTS</span></span>

### <span data-ttu-id="62232-138">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="62232-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="62232-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62232-139">NOTES</span></span>

## <span data-ttu-id="62232-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62232-140">RELATED LINKS</span></span>

[<span data-ttu-id="62232-141">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="62232-141">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="62232-142">Új – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="62232-142">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="62232-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="62232-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


