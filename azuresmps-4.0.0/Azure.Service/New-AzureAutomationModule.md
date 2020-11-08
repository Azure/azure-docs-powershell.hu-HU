---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016223"
---
# <span data-ttu-id="05e25-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05e25-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="05e25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05e25-102">SYNOPSIS</span></span>

<span data-ttu-id="05e25-103">Modul importálása automatizálásra.</span><span class="sxs-lookup"><span data-stu-id="05e25-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="05e25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05e25-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05e25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05e25-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="05e25-106">A **New-AzureAutomationModule** parancsmag modult importál az Azure automatizálásba.</span><span class="sxs-lookup"><span data-stu-id="05e25-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="05e25-107">A modul egy. zip kiterjesztésű tömörített fájl, amely egy olyan mappát tartalmaz, amely az alábbi fájltípusok egyikét tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="05e25-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="05e25-108">Windows PowerShell-modul (psm1-fájl)</span><span class="sxs-lookup"><span data-stu-id="05e25-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="05e25-109">Windows PowerShell-modul jegyzékfájlja (psd1-fájl)</span><span class="sxs-lookup"><span data-stu-id="05e25-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="05e25-110">Egy kódösszeállítás (dll-fájl)</span><span class="sxs-lookup"><span data-stu-id="05e25-110">An assembly (dll file).</span></span>

<span data-ttu-id="05e25-111">A zip-fájl, a zip-fájl mappája és a mappában lévő fájl (. psm1, PSD. 1 vagy. dll) neveinek egyezniük kell.</span><span class="sxs-lookup"><span data-stu-id="05e25-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="05e25-112">Példák</span><span class="sxs-lookup"><span data-stu-id="05e25-112">EXAMPLES</span></span>

### <span data-ttu-id="05e25-113">1. példa: modul importálása</span><span class="sxs-lookup"><span data-stu-id="05e25-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="05e25-114">Ez a parancs a ContosoModule nevű modult importálja a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="05e25-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="05e25-115">A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.</span><span class="sxs-lookup"><span data-stu-id="05e25-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="05e25-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05e25-116">PARAMETERS</span></span>

### <span data-ttu-id="05e25-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05e25-117">-AutomationAccountName</span></span>
<span data-ttu-id="05e25-118">Annak az automatizálási fióknak a neve, amelyet a modul tárol.</span><span class="sxs-lookup"><span data-stu-id="05e25-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e25-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="05e25-119">-ContentLink</span></span>
<span data-ttu-id="05e25-120">Nyilvános URL-cím, például webhely vagy Azure Blob-tárhely, amely a modul elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05e25-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="05e25-121">Ennek a helynek nyilvánosan elérhetőnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="05e25-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e25-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05e25-122">-Name</span></span>
<span data-ttu-id="05e25-123">A modul nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05e25-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e25-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="05e25-124">-Profile</span></span>
<span data-ttu-id="05e25-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="05e25-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05e25-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="05e25-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e25-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="05e25-127">-Tags</span></span>
<span data-ttu-id="05e25-128">Egy vagy több, a modulhoz kapcsolódó címkét ad meg.</span><span class="sxs-lookup"><span data-stu-id="05e25-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e25-129">CommonParameters</span></span>
<span data-ttu-id="05e25-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05e25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e25-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e25-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e25-132">INPUTS</span></span>

## <span data-ttu-id="05e25-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e25-133">OUTPUTS</span></span>

### <span data-ttu-id="05e25-134">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="05e25-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="05e25-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05e25-135">NOTES</span></span>

## <span data-ttu-id="05e25-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05e25-136">RELATED LINKS</span></span>

[<span data-ttu-id="05e25-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05e25-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="05e25-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05e25-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="05e25-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05e25-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


