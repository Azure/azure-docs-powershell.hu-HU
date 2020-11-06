---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501547"
---
# <span data-ttu-id="9500e-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="9500e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9500e-102">SYNOPSIS</span></span>
<span data-ttu-id="9500e-103">Módosítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="9500e-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9500e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9500e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9500e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9500e-105">DESCRIPTION</span></span>
<span data-ttu-id="9500e-106">A **set-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook konfigurációját módosítja az APS-ben.</span><span class="sxs-lookup"><span data-stu-id="9500e-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="9500e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9500e-107">EXAMPLES</span></span>

### <span data-ttu-id="9500e-108">Példa 1: a runbook részletes naplózásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="9500e-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9500e-109">Ez a parancs lehetővé teszi a részletes naplózást a megadott runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9500e-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9500e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9500e-110">PARAMETERS</span></span>

### <span data-ttu-id="9500e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9500e-111">-AutomationAccountName</span></span>
<span data-ttu-id="9500e-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag módosította a runbook.</span><span class="sxs-lookup"><span data-stu-id="9500e-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="9500e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9500e-113">-DefaultProfile</span></span>
<span data-ttu-id="9500e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9500e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9500e-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9500e-115">-Description</span></span>
<span data-ttu-id="9500e-116">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9500e-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="9500e-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="9500e-117">-LogProgress</span></span>
<span data-ttu-id="9500e-118">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="9500e-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9500e-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="9500e-119">-LogVerbose</span></span>
<span data-ttu-id="9500e-120">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="9500e-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9500e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9500e-121">-Name</span></span>
<span data-ttu-id="9500e-122">Annak a runbook a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="9500e-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9500e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9500e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9500e-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag módosított egy runbook.</span><span class="sxs-lookup"><span data-stu-id="9500e-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="9500e-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="9500e-125">-Tag</span></span>
<span data-ttu-id="9500e-126">A runbook címkék.</span><span class="sxs-lookup"><span data-stu-id="9500e-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9500e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9500e-127">CommonParameters</span></span>
<span data-ttu-id="9500e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9500e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9500e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9500e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9500e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9500e-130">INPUTS</span></span>

### <span data-ttu-id="9500e-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="9500e-131">None</span></span>
<span data-ttu-id="9500e-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9500e-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9500e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9500e-133">OUTPUTS</span></span>

### <span data-ttu-id="9500e-134">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="9500e-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9500e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9500e-135">NOTES</span></span>

## <span data-ttu-id="9500e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9500e-136">RELATED LINKS</span></span>

[<span data-ttu-id="9500e-137">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-139">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-140">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-141">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-142">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9500e-144">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9500e-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


