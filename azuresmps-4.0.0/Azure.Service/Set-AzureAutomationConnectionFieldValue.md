---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016427"
---
# <span data-ttu-id="9e095-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9e095-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="9e095-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e095-102">SYNOPSIS</span></span>

<span data-ttu-id="9e095-103">Egy kapcsolat mezőinek értékét módosítja.</span><span class="sxs-lookup"><span data-stu-id="9e095-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="9e095-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e095-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e095-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e095-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9e095-106">A **set-AzureAutomationConnectionFieldValue** parancsmag módosította egy mező értékét az Azure automatizálásban való kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="9e095-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="9e095-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e095-107">EXAMPLES</span></span>

## <span data-ttu-id="9e095-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e095-108">PARAMETERS</span></span>

### <span data-ttu-id="9e095-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e095-109">-AutomationAccountName</span></span>
<span data-ttu-id="9e095-110">Megadja a kapcsolat automatizálási fiókjának a nevét.</span><span class="sxs-lookup"><span data-stu-id="9e095-110">Specifies the name of the Automation account with the connection.</span></span>

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

### <span data-ttu-id="9e095-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="9e095-111">-ConnectionFieldName</span></span>
<span data-ttu-id="9e095-112">A mező nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e095-112">Specifies a name for the field.</span></span>

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

### <span data-ttu-id="9e095-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e095-113">-Name</span></span>
<span data-ttu-id="9e095-114">A kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e095-114">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="9e095-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e095-115">-Profile</span></span>
<span data-ttu-id="9e095-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9e095-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e095-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9e095-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e095-118">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="9e095-118">-Value</span></span>
<span data-ttu-id="9e095-119">A kapcsolat mezőben a tárolandó értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e095-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e095-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e095-120">CommonParameters</span></span>
<span data-ttu-id="9e095-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e095-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e095-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e095-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e095-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e095-123">INPUTS</span></span>

## <span data-ttu-id="9e095-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e095-124">OUTPUTS</span></span>

## <span data-ttu-id="9e095-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e095-125">NOTES</span></span>

## <span data-ttu-id="9e095-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e095-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e095-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9e095-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="9e095-128">Új – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9e095-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="9e095-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9e095-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


