---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016371"
---
# <span data-ttu-id="7d0f7-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7d0f7-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="7d0f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d0f7-102">SYNOPSIS</span></span>

<span data-ttu-id="7d0f7-103">Azure automatizálási fiókokat kap.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="7d0f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d0f7-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d0f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d0f7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7d0f7-106">A **Get-AzureAutomationAccount** parancsmag a Microsoft Azure automatizálási fiókokat kapja az előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="7d0f7-107">Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="7d0f7-108">Az automatizálási erőforrások közé tartozik a runbooks, a feladatok és az eszközök.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="7d0f7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d0f7-109">EXAMPLES</span></span>

### <span data-ttu-id="7d0f7-110">Példa 1: automatizálási fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="7d0f7-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="7d0f7-111">Ez a parancs a Contoso17 nevű automatizálási fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7d0f7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d0f7-112">PARAMETERS</span></span>

### <span data-ttu-id="7d0f7-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="7d0f7-113">-Location</span></span>
<span data-ttu-id="7d0f7-114">Az automatizálási fiókokkal társított Azure-helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-114">Specifies an Azure location associated with Automation accounts.</span></span>

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

### <span data-ttu-id="7d0f7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d0f7-115">-Name</span></span>
<span data-ttu-id="7d0f7-116">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0f7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d0f7-117">-Profile</span></span>
<span data-ttu-id="7d0f7-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d0f7-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7d0f7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d0f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0f7-120">CommonParameters</span></span>
<span data-ttu-id="7d0f7-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d0f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0f7-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0f7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0f7-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d0f7-123">INPUTS</span></span>

## <span data-ttu-id="7d0f7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d0f7-124">OUTPUTS</span></span>

### <span data-ttu-id="7d0f7-125">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7d0f7-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7d0f7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d0f7-126">NOTES</span></span>

## <span data-ttu-id="7d0f7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d0f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="7d0f7-128">Új – AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7d0f7-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="7d0f7-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7d0f7-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


