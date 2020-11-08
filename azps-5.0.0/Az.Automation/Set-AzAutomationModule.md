---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187084"
---
# <span data-ttu-id="78ac3-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="78ac3-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="78ac3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="78ac3-103">Frissít egy modult az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="78ac3-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="78ac3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78ac3-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78ac3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="78ac3-106">A **set-AzAutomationModule** parancsmag az Azure automatizálás modulban frissíti a modult.</span><span class="sxs-lookup"><span data-stu-id="78ac3-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="78ac3-107">Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.</span><span class="sxs-lookup"><span data-stu-id="78ac3-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="78ac3-108">A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="78ac3-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="78ac3-109">wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van</span><span class="sxs-lookup"><span data-stu-id="78ac3-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="78ac3-110">wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel): a. zip fájl neve, a mappa neve és a mappában lévő fájl neve kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="78ac3-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="78ac3-111">Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.</span><span class="sxs-lookup"><span data-stu-id="78ac3-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="78ac3-112">Ha a parancsmaggal vagy a New-AzAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.</span><span class="sxs-lookup"><span data-stu-id="78ac3-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="78ac3-113">A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="78ac3-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="78ac3-114">Annak ellenőrzéséhez, hogy sikerült-e, futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName ellenőrizze a **ProvisioningState** tulajdonság értékét a sikeres érték eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="78ac3-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="78ac3-115">Példák</span><span class="sxs-lookup"><span data-stu-id="78ac3-115">EXAMPLES</span></span>

### <span data-ttu-id="78ac3-116">Példa 1: modul frissítése</span><span class="sxs-lookup"><span data-stu-id="78ac3-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="78ac3-117">Ez a parancs a ContosoModule nevű meglévő modul frissített verzióját importálja a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="78ac3-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="78ac3-118">A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="78ac3-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="78ac3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78ac3-119">PARAMETERS</span></span>

### <span data-ttu-id="78ac3-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78ac3-120">-AutomationAccountName</span></span>
<span data-ttu-id="78ac3-121">Annak az automatizálási fióknak a neve, amelyhez a parancsmag egy modult frissít.</span><span class="sxs-lookup"><span data-stu-id="78ac3-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="78ac3-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="78ac3-122">-ContentLinkUri</span></span>
<span data-ttu-id="78ac3-123">Annak a. zip fájlnak az URL-címét adja meg, amely a parancsmag által importált modul új verzióját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="78ac3-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="78ac3-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="78ac3-124">-ContentLinkVersion</span></span>
<span data-ttu-id="78ac3-125">Annak a modulnak a verziója, amelyre ez a parancsmag frissíti az automatizálást.</span><span class="sxs-lookup"><span data-stu-id="78ac3-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="78ac3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ac3-126">-DefaultProfile</span></span>
<span data-ttu-id="78ac3-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78ac3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78ac3-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78ac3-128">-Name</span></span>
<span data-ttu-id="78ac3-129">Annak a modulnak a nevét adja meg, amelyre a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="78ac3-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="78ac3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ac3-130">-ResourceGroupName</span></span>
<span data-ttu-id="78ac3-131">Annak a csoportnak a neve, amelyhez a parancsmag egy modult frissít.</span><span class="sxs-lookup"><span data-stu-id="78ac3-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="78ac3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ac3-132">CommonParameters</span></span>
<span data-ttu-id="78ac3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78ac3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ac3-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ac3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ac3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78ac3-135">INPUTS</span></span>

### <span data-ttu-id="78ac3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="78ac3-136">System.String</span></span>

### <span data-ttu-id="78ac3-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="78ac3-137">System.Uri</span></span>

## <span data-ttu-id="78ac3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78ac3-138">OUTPUTS</span></span>

### <span data-ttu-id="78ac3-139">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="78ac3-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="78ac3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78ac3-140">NOTES</span></span>

## <span data-ttu-id="78ac3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78ac3-141">RELATED LINKS</span></span>

[<span data-ttu-id="78ac3-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="78ac3-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="78ac3-143">Új – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="78ac3-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="78ac3-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="78ac3-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

