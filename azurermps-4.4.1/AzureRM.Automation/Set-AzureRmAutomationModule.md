---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493873"
---
# <span data-ttu-id="7a17b-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7a17b-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="7a17b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a17b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a17b-103">Frissít egy modult az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="7a17b-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a17b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a17b-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a17b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a17b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a17b-106">A **set-AzureRmAutomationModule** parancsmag az Azure automatizálás modulban frissíti a modult.</span><span class="sxs-lookup"><span data-stu-id="7a17b-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="7a17b-107">Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.</span><span class="sxs-lookup"><span data-stu-id="7a17b-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="7a17b-108">A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="7a17b-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="7a17b-109">wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van</span><span class="sxs-lookup"><span data-stu-id="7a17b-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="7a17b-110">wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel)</span><span class="sxs-lookup"><span data-stu-id="7a17b-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="7a17b-111">A. zip fájl neve, a mappa neve és a mappa fájlnevének egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="7a17b-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="7a17b-112">Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.</span><span class="sxs-lookup"><span data-stu-id="7a17b-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="7a17b-113">Ha a parancsmaggal vagy a New-AzureRmAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.</span><span class="sxs-lookup"><span data-stu-id="7a17b-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="7a17b-114">A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.</span><span class="sxs-lookup"><span data-stu-id="7a17b-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="7a17b-115">A következő parancs futtatásával ellenőrizheti, hogy sikerült-e:</span><span class="sxs-lookup"><span data-stu-id="7a17b-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="7a17b-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="7a17b-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="7a17b-117">Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="7a17b-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="7a17b-118">Példák</span><span class="sxs-lookup"><span data-stu-id="7a17b-118">EXAMPLES</span></span>

### <span data-ttu-id="7a17b-119">Példa 1: modul frissítése</span><span class="sxs-lookup"><span data-stu-id="7a17b-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7a17b-120">Ez a parancs a ContosoModule nevű meglévő modul frissített verzióját importálja a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="7a17b-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7a17b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a17b-121">PARAMETERS</span></span>

### <span data-ttu-id="7a17b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a17b-122">-AutomationAccountName</span></span>
<span data-ttu-id="7a17b-123">Annak az automatizálási fióknak a neve, amelyhez a parancsmag egy modult frissít.</span><span class="sxs-lookup"><span data-stu-id="7a17b-123">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7a17b-124">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="7a17b-124">-ContentLinkUri</span></span>
<span data-ttu-id="7a17b-125">Annak a. zip fájlnak az URL-címét adja meg, amely a parancsmag által importált modul új verzióját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7a17b-125">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7a17b-126">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="7a17b-126">-ContentLinkVersion</span></span>
<span data-ttu-id="7a17b-127">Annak a modulnak a verziója, amelyre ez a parancsmag frissíti az automatizálást.</span><span class="sxs-lookup"><span data-stu-id="7a17b-127">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="7a17b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a17b-128">-Name</span></span>
<span data-ttu-id="7a17b-129">Annak a modulnak a nevét adja meg, amelyre a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="7a17b-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7a17b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a17b-130">-ResourceGroupName</span></span>
<span data-ttu-id="7a17b-131">Annak a csoportnak a neve, amelyhez a parancsmag egy modult frissít.</span><span class="sxs-lookup"><span data-stu-id="7a17b-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7a17b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a17b-132">-DefaultProfile</span></span>
<span data-ttu-id="7a17b-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a17b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a17b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a17b-134">CommonParameters</span></span>
<span data-ttu-id="7a17b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a17b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a17b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a17b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a17b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a17b-137">INPUTS</span></span>

## <span data-ttu-id="7a17b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a17b-138">OUTPUTS</span></span>

### <span data-ttu-id="7a17b-139">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="7a17b-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="7a17b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a17b-140">NOTES</span></span>

## <span data-ttu-id="7a17b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a17b-141">RELATED LINKS</span></span>

[<span data-ttu-id="7a17b-142">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7a17b-142">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="7a17b-143">Új – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7a17b-143">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="7a17b-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7a17b-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


