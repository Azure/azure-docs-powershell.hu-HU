---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373056"
---
# <span data-ttu-id="acc8c-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="acc8c-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="acc8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="acc8c-103">Frissíti a modult az Automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="acc8c-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="acc8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acc8c-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acc8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acc8c-105">DESCRIPTION</span></span>
<span data-ttu-id="acc8c-106">A **Set-AzAutomationModule** parancsmag frissíti az Azure Automation egyik modulját.</span><span class="sxs-lookup"><span data-stu-id="acc8c-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="acc8c-107">Ez a parancs elfogad egy .zip kiterjesztésű tömörített fájlt.</span><span class="sxs-lookup"><span data-stu-id="acc8c-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="acc8c-108">A fájl egy mappát tartalmaz, amely az alábbi típusú fájlok egyikét tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="acc8c-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="acc8c-109">wps_2 .psm1 vagy .dll kiterjesztésű modul</span><span class="sxs-lookup"><span data-stu-id="acc8c-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="acc8c-110">wps_2 .psd1 kiterjesztésű modul jegyzékfájljának. A .zip fájlnak, a mappa nevének és a mappában lévő fájl nevének meg kell egynie.</span><span class="sxs-lookup"><span data-stu-id="acc8c-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="acc8c-111">Adja meg a .zip fájlt URL-címként, amelyhez az automatizálási szolgáltatás hozzáférhet.</span><span class="sxs-lookup"><span data-stu-id="acc8c-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="acc8c-112">Ha ezzel a wps_2 vagy a New-AzAutomationModule parancsmag használatával importál egy modult az automatizálásba, a művelet aszinkron lesz.</span><span class="sxs-lookup"><span data-stu-id="acc8c-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="acc8c-113">A parancs befejezi, hogy az importálás sikeres-e vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="acc8c-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="acc8c-114">A sikeres ellenőrzéshez futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke Sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="acc8c-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="acc8c-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acc8c-115">EXAMPLES</span></span>

### <span data-ttu-id="acc8c-116">1. példa: Modul frissítése</span><span class="sxs-lookup"><span data-stu-id="acc8c-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="acc8c-117">Ez a parancs importálja egy ContosoModule nevű meglévő modul frissített verzióját a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="acc8c-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="acc8c-118">A modult egy Azure-blob tárolja egy contosostorage nevű tárfiókban és egy modulnak nevezett tárolóban.</span><span class="sxs-lookup"><span data-stu-id="acc8c-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="acc8c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc8c-119">PARAMETERS</span></span>

### <span data-ttu-id="acc8c-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="acc8c-120">-AutomationAccountName</span></span>
<span data-ttu-id="acc8c-121">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja frissíti a modult.</span><span class="sxs-lookup"><span data-stu-id="acc8c-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="acc8c-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="acc8c-122">-ContentLinkUri</span></span>
<span data-ttu-id="acc8c-123">Annak a .zip fájlnak az URL-címét adja meg, amely a parancsmag által importálni kívánt modul új verzióját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="acc8c-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc8c-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="acc8c-124">-ContentLinkVersion</span></span>
<span data-ttu-id="acc8c-125">Annak a modulnak a verzióját adja meg, amelyre ez a parancsmag frissíti az Automatizálást.</span><span class="sxs-lookup"><span data-stu-id="acc8c-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="acc8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc8c-126">-DefaultProfile</span></span>
<span data-ttu-id="acc8c-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="acc8c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acc8c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="acc8c-128">-Name</span></span>
<span data-ttu-id="acc8c-129">Annak a modulnak a nevét adja meg, amelyből a parancsmag importálja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="acc8c-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="acc8c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc8c-130">-ResourceGroupName</span></span>
<span data-ttu-id="acc8c-131">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja frissíti a modult.</span><span class="sxs-lookup"><span data-stu-id="acc8c-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="acc8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc8c-132">CommonParameters</span></span>
<span data-ttu-id="acc8c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc8c-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc8c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc8c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acc8c-135">INPUTS</span></span>

### <span data-ttu-id="acc8c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="acc8c-136">System.String</span></span>

### <span data-ttu-id="acc8c-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="acc8c-137">System.Uri</span></span>

## <span data-ttu-id="acc8c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc8c-138">OUTPUTS</span></span>

### <span data-ttu-id="acc8c-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="acc8c-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="acc8c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acc8c-140">NOTES</span></span>

## <span data-ttu-id="acc8c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acc8c-141">RELATED LINKS</span></span>

[<span data-ttu-id="acc8c-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="acc8c-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="acc8c-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="acc8c-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="acc8c-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="acc8c-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


