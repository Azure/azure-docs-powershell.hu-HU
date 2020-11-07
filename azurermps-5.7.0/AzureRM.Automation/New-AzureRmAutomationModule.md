---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672176"
---
# <span data-ttu-id="b87ec-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b87ec-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="b87ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b87ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b87ec-103">Modul importálása automatizálásra.</span><span class="sxs-lookup"><span data-stu-id="b87ec-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b87ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b87ec-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b87ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b87ec-105">DESCRIPTION</span></span>
<span data-ttu-id="b87ec-106">A **New-AzureRmAutomationModule** parancsmag modult importál az Azure automatizálásba.</span><span class="sxs-lookup"><span data-stu-id="b87ec-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="b87ec-107">Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.</span><span class="sxs-lookup"><span data-stu-id="b87ec-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="b87ec-108">A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="b87ec-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="b87ec-109">wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van</span><span class="sxs-lookup"><span data-stu-id="b87ec-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="b87ec-110">wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel)</span><span class="sxs-lookup"><span data-stu-id="b87ec-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="b87ec-111">A. zip fájl neve, a mappa neve és a mappa fájlnevének egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="b87ec-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="b87ec-112">Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.</span><span class="sxs-lookup"><span data-stu-id="b87ec-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="b87ec-113">Ha a parancsmaggal vagy a Set-AzureRmAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.</span><span class="sxs-lookup"><span data-stu-id="b87ec-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="b87ec-114">A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="b87ec-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="b87ec-115">A következő parancs futtatásával ellenőrizheti, hogy sikerült-e:</span><span class="sxs-lookup"><span data-stu-id="b87ec-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="b87ec-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="b87ec-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="b87ec-117">Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="b87ec-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="b87ec-118">Példák</span><span class="sxs-lookup"><span data-stu-id="b87ec-118">EXAMPLES</span></span>

### <span data-ttu-id="b87ec-119">1. példa: modul importálása</span><span class="sxs-lookup"><span data-stu-id="b87ec-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b87ec-120">Ez a parancs a ContosoModule nevű modult importálja a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="b87ec-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="b87ec-121">A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="b87ec-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="b87ec-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b87ec-122">PARAMETERS</span></span>

### <span data-ttu-id="b87ec-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b87ec-123">-AutomationAccountName</span></span>
<span data-ttu-id="b87ec-124">Annak az automatizálási fióknak a neve, amelyhez a parancsmag modult importál.</span><span class="sxs-lookup"><span data-stu-id="b87ec-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="b87ec-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="b87ec-125">-ContentLinkUri</span></span>
<span data-ttu-id="b87ec-126">A modul ZIP-csomagjának URL-címe</span><span class="sxs-lookup"><span data-stu-id="b87ec-126">The url to a module zip package</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87ec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87ec-127">-DefaultProfile</span></span>
<span data-ttu-id="b87ec-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b87ec-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b87ec-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b87ec-129">-Name</span></span>
<span data-ttu-id="b87ec-130">Annak a modulnak a nevét adja meg, amelyre a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="b87ec-130">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="b87ec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b87ec-131">-ResourceGroupName</span></span>
<span data-ttu-id="b87ec-132">Annak az erőforráscsoport a nevét adja meg, amelyhez a parancsmag modult importál.</span><span class="sxs-lookup"><span data-stu-id="b87ec-132">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="b87ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87ec-133">CommonParameters</span></span>
<span data-ttu-id="b87ec-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b87ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87ec-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b87ec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87ec-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b87ec-136">INPUTS</span></span>

### <span data-ttu-id="b87ec-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="b87ec-137">None</span></span>
<span data-ttu-id="b87ec-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b87ec-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b87ec-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b87ec-139">OUTPUTS</span></span>

### <span data-ttu-id="b87ec-140">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="b87ec-140">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="b87ec-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b87ec-141">NOTES</span></span>

## <span data-ttu-id="b87ec-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b87ec-142">RELATED LINKS</span></span>

[<span data-ttu-id="b87ec-143">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b87ec-143">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="b87ec-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b87ec-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="b87ec-145">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="b87ec-145">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


