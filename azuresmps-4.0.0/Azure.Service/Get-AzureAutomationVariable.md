---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015653"
---
# <span data-ttu-id="9a101-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a101-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="9a101-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a101-102">SYNOPSIS</span></span>

<span data-ttu-id="9a101-103">Automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="9a101-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="9a101-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a101-104">SYNTAX</span></span>

### <span data-ttu-id="9a101-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a101-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9a101-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9a101-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a101-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a101-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9a101-108">A **Get-AzureAutomationVariable** parancsmag egy vagy több Microsoft Azure automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="9a101-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="9a101-109">Alapértelmezés szerint minden változót visszaad a függvény.</span><span class="sxs-lookup"><span data-stu-id="9a101-109">By default, all variables are returned.</span></span>
<span data-ttu-id="9a101-110">Ha meghatározott változót szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="9a101-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="9a101-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9a101-111">EXAMPLES</span></span>

### <span data-ttu-id="9a101-112">Példa 1: változó beszerzése</span><span class="sxs-lookup"><span data-stu-id="9a101-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="9a101-113">Ezekkel a parancsokkal egy MyVariable nevű automatizálási változót kap, és az értéket hozzárendeli egy $value nevű változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9a101-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="9a101-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a101-114">PARAMETERS</span></span>

### <span data-ttu-id="9a101-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a101-115">-AutomationAccountName</span></span>
<span data-ttu-id="9a101-116">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a101-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="9a101-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a101-117">-Name</span></span>
<span data-ttu-id="9a101-118">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a101-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a101-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9a101-119">-Profile</span></span>
<span data-ttu-id="9a101-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9a101-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a101-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9a101-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a101-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a101-122">CommonParameters</span></span>
<span data-ttu-id="9a101-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a101-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a101-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a101-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a101-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a101-125">INPUTS</span></span>

## <span data-ttu-id="9a101-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a101-126">OUTPUTS</span></span>

### <span data-ttu-id="9a101-127">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="9a101-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="9a101-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a101-128">NOTES</span></span>

## <span data-ttu-id="9a101-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a101-129">RELATED LINKS</span></span>

[<span data-ttu-id="9a101-130">Új – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a101-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="9a101-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a101-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="9a101-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9a101-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


