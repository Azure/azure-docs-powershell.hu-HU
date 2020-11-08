---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016224"
---
# <span data-ttu-id="eb474-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eb474-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="eb474-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb474-102">SYNOPSIS</span></span>

<span data-ttu-id="eb474-103">Automatizálási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eb474-103">Creates an Automation account.</span></span>

## <span data-ttu-id="eb474-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb474-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb474-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb474-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="eb474-106">A **New-AzureAutomationAccount** parancsmag új fiókot hoz létre a Microsoft Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="eb474-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="eb474-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb474-107">EXAMPLES</span></span>

### <span data-ttu-id="eb474-108">Példa 1: automatizálási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="eb474-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="eb474-109">Ez a parancs létrehoz egy MyAutomationAccount nevű automatizálási fiókot a kelet-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="eb474-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="eb474-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb474-110">PARAMETERS</span></span>

### <span data-ttu-id="eb474-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb474-111">-Location</span></span>
<span data-ttu-id="eb474-112">A fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb474-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="eb474-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb474-113">-Name</span></span>
<span data-ttu-id="eb474-114">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb474-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb474-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb474-115">-Profile</span></span>
<span data-ttu-id="eb474-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="eb474-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb474-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="eb474-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb474-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb474-118">CommonParameters</span></span>
<span data-ttu-id="eb474-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb474-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb474-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb474-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb474-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb474-121">INPUTS</span></span>

## <span data-ttu-id="eb474-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb474-122">OUTPUTS</span></span>

### <span data-ttu-id="eb474-123">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eb474-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="eb474-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb474-124">NOTES</span></span>

## <span data-ttu-id="eb474-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb474-125">RELATED LINKS</span></span>

[<span data-ttu-id="eb474-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eb474-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="eb474-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="eb474-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


