---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015830"
---
# <span data-ttu-id="d15b2-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d15b2-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="d15b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d15b2-102">SYNOPSIS</span></span>

<span data-ttu-id="d15b2-103">Frissít egy modult az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d15b2-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="d15b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d15b2-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d15b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d15b2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d15b2-106">A **set-AzureAutomationModule** parancsmag a modul új verzióját importálja, vagy módosítja a modul konfigurációját az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d15b2-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="d15b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d15b2-107">EXAMPLES</span></span>

### <span data-ttu-id="d15b2-108">Példa 1: modul frissítése</span><span class="sxs-lookup"><span data-stu-id="d15b2-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="d15b2-109">Ez a parancs a ContosoModule nevű meglévő modul frissített verzióját importálja a Contoso17 nevű Azure automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="d15b2-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d15b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d15b2-110">PARAMETERS</span></span>

### <span data-ttu-id="d15b2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d15b2-111">-AutomationAccountName</span></span>
<span data-ttu-id="d15b2-112">A modulhoz tartozó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d15b2-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="d15b2-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="d15b2-113">-ContentLinkUri</span></span>
<span data-ttu-id="d15b2-114">A Module-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d15b2-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d15b2-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="d15b2-115">-ContentLinkVersion</span></span>
<span data-ttu-id="d15b2-116">A modul verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d15b2-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="d15b2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d15b2-117">-Name</span></span>
<span data-ttu-id="d15b2-118">A modul nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d15b2-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="d15b2-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="d15b2-119">-Profile</span></span>
<span data-ttu-id="d15b2-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d15b2-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d15b2-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d15b2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d15b2-122">-Címkék</span><span class="sxs-lookup"><span data-stu-id="d15b2-122">-Tags</span></span>
<span data-ttu-id="d15b2-123">A modul címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="d15b2-123">Specifies tags for the module.</span></span>

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

### <span data-ttu-id="d15b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15b2-124">CommonParameters</span></span>
<span data-ttu-id="d15b2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d15b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15b2-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15b2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d15b2-127">INPUTS</span></span>

### <span data-ttu-id="d15b2-128">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="d15b2-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d15b2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d15b2-129">OUTPUTS</span></span>

## <span data-ttu-id="d15b2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d15b2-130">NOTES</span></span>

## <span data-ttu-id="d15b2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d15b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="d15b2-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d15b2-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="d15b2-133">Új – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d15b2-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="d15b2-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d15b2-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


