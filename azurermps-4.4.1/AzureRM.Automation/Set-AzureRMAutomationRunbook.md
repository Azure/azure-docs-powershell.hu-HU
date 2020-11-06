---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493882"
---
# <span data-ttu-id="3cb6a-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="3cb6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb6a-103">Módosítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cb6a-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb6a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb6a-106">A **set-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook konfigurációját módosítja az APS-ben.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="3cb6a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3cb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb6a-108">Példa 1: a runbook részletes naplózásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="3cb6a-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3cb6a-109">Ez a parancs lehetővé teszi a részletes naplózást a megadott runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3cb6a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cb6a-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb6a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3cb6a-111">-AutomationAccountName</span></span>
<span data-ttu-id="3cb6a-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag módosította a runbook.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3cb6a-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3cb6a-113">-Description</span></span>
<span data-ttu-id="3cb6a-114">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="3cb6a-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="3cb6a-115">-LogProgress</span></span>
<span data-ttu-id="3cb6a-116">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb6a-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3cb6a-117">-LogVerbose</span></span>
<span data-ttu-id="3cb6a-118">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb6a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cb6a-119">-Name</span></span>
<span data-ttu-id="3cb6a-120">Annak a runbook a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cb6a-122">Annak az erőforráscsoport a neve, amelyhez a parancsmag módosított egy runbook.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3cb6a-123">-Címkék</span><span class="sxs-lookup"><span data-stu-id="3cb6a-123">-Tags</span></span>
<span data-ttu-id="3cb6a-124">A címkék szótárát adja vissza a módosított runbook aktuális címkéit.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb6a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb6a-125">-DefaultProfile</span></span>
<span data-ttu-id="3cb6a-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb6a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb6a-127">CommonParameters</span></span>
<span data-ttu-id="3cb6a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cb6a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb6a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb6a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb6a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cb6a-130">INPUTS</span></span>

## <span data-ttu-id="3cb6a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cb6a-131">OUTPUTS</span></span>

### <span data-ttu-id="3cb6a-132">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="3cb6a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cb6a-133">NOTES</span></span>

## <span data-ttu-id="3cb6a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cb6a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3cb6a-135">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-137">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-138">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-139">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-140">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3cb6a-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3cb6a-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


