---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016484"
---
# <span data-ttu-id="8d0e8-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="8d0e8-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="8d0e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d0e8-102">SYNOPSIS</span></span>

<span data-ttu-id="8d0e8-103">Kapcsolat típusának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8d0e8-103">Removes a connection type.</span></span>

## <span data-ttu-id="8d0e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d0e8-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d0e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d0e8-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8d0e8-106">A **Remove-AzureAutomationConnectionType** parancsmag eltávolítja az Azure automatizálási kapcsolat típusát.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="8d0e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d0e8-107">EXAMPLES</span></span>

## <span data-ttu-id="8d0e8-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d0e8-108">PARAMETERS</span></span>

### <span data-ttu-id="8d0e8-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d0e8-109">-AutomationAccountName</span></span>
<span data-ttu-id="8d0e8-110">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="8d0e8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8d0e8-111">-Force</span></span>
<span data-ttu-id="8d0e8-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0e8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d0e8-113">-Name</span></span>
<span data-ttu-id="8d0e8-114">Az eltávolítandó kapcsolattípus nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="8d0e8-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d0e8-115">-Profile</span></span>
<span data-ttu-id="8d0e8-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d0e8-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8d0e8-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d0e8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0e8-118">CommonParameters</span></span>
<span data-ttu-id="8d0e8-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d0e8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0e8-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d0e8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0e8-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d0e8-121">INPUTS</span></span>

## <span data-ttu-id="8d0e8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d0e8-122">OUTPUTS</span></span>

## <span data-ttu-id="8d0e8-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d0e8-123">NOTES</span></span>

## <span data-ttu-id="8d0e8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d0e8-124">RELATED LINKS</span></span>

