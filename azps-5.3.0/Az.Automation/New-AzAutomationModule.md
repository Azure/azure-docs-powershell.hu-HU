---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478617"
---
# <span data-ttu-id="cd953-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cd953-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="cd953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd953-102">SYNOPSIS</span></span>
<span data-ttu-id="cd953-103">Modult importál az automatizálásba.</span><span class="sxs-lookup"><span data-stu-id="cd953-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="cd953-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd953-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd953-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd953-105">DESCRIPTION</span></span>
<span data-ttu-id="cd953-106">A **New-AzAutomationModule** parancsmag egy modult importál az Azure Automatizálásba.</span><span class="sxs-lookup"><span data-stu-id="cd953-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="cd953-107">Ez a parancs elfogad egy .zip kiterjesztésű tömörített fájlt.</span><span class="sxs-lookup"><span data-stu-id="cd953-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="cd953-108">A fájl egy mappát tartalmaz, amely az alábbi típusú fájlok egyikét tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="cd953-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="cd953-109">Windows PowerShell-modul, amelynek .psm1 vagy .dll fájlnévkiterjesztése van</span><span class="sxs-lookup"><span data-stu-id="cd953-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="cd953-110">A Windows PowerShell-modul jegyzékfájljának .psd1 fájlnévkiterjesztéssel, a .zip fájl nevével, a mappa nevével és a mappában lévő fájl nevével azonosnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="cd953-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="cd953-111">Adja meg a .zip fájlt URL-címként, amelyhez az automatizálási szolgáltatás hozzáférhet.</span><span class="sxs-lookup"><span data-stu-id="cd953-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="cd953-112">Ha ezzel a parancsmagmal vagy a Set-AzAutomationModule parancsmag használatával importál egy Windows PowerShell-modult az automatizálásba, a művelet aszinkron lesz.</span><span class="sxs-lookup"><span data-stu-id="cd953-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="cd953-113">A parancs befejezi, hogy az importálás sikeres-e vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="cd953-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="cd953-114">A sikeres ellenőrzéshez futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke Sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="cd953-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="cd953-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd953-115">EXAMPLES</span></span>

### <span data-ttu-id="cd953-116">1. példa: Modul importálása</span><span class="sxs-lookup"><span data-stu-id="cd953-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd953-117">Ez a parancs importálja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="cd953-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="cd953-118">A modult egy Azure-blob tárolja egy contosostorage nevű tárfiókban és egy modulnak nevezett tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cd953-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="cd953-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd953-119">PARAMETERS</span></span>

### <span data-ttu-id="cd953-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd953-120">-AutomationAccountName</span></span>
<span data-ttu-id="cd953-121">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja importál egy modult.</span><span class="sxs-lookup"><span data-stu-id="cd953-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="cd953-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="cd953-122">-ContentLinkUri</span></span>
<span data-ttu-id="cd953-123">A modul zip csomag url-címe</span><span class="sxs-lookup"><span data-stu-id="cd953-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd953-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd953-124">-DefaultProfile</span></span>
<span data-ttu-id="cd953-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd953-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd953-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cd953-126">-Name</span></span>
<span data-ttu-id="cd953-127">Annak a modulnak a nevét adja meg, amelyből a parancsmag importálja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd953-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="cd953-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd953-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd953-129">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja egy modult importál.</span><span class="sxs-lookup"><span data-stu-id="cd953-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="cd953-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd953-130">CommonParameters</span></span>
<span data-ttu-id="cd953-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd953-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd953-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd953-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd953-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd953-133">INPUTS</span></span>

### <span data-ttu-id="cd953-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cd953-134">System.String</span></span>

### <span data-ttu-id="cd953-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="cd953-135">System.Uri</span></span>

## <span data-ttu-id="cd953-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd953-136">OUTPUTS</span></span>

### <span data-ttu-id="cd953-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="cd953-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="cd953-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd953-138">NOTES</span></span>

## <span data-ttu-id="cd953-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd953-139">RELATED LINKS</span></span>

[<span data-ttu-id="cd953-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cd953-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="cd953-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cd953-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="cd953-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cd953-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


