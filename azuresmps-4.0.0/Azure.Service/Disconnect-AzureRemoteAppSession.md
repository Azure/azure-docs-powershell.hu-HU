---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015686"
---
# <span data-ttu-id="9fa45-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="9fa45-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="9fa45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fa45-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa45-103">Leválasztja az Azure RemoteApp-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="9fa45-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="9fa45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fa45-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fa45-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa45-106">A **leválasztási AzureRemoteAppSession** parancsmag leválasztja a felhasználó Azure RemoteApp-munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="9fa45-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="9fa45-107">A felhasználó ügyfele leválasztja az Azure RemoteApp-munkamenetét, de a felhasználó programjai továbbra is futnak.</span><span class="sxs-lookup"><span data-stu-id="9fa45-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="9fa45-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9fa45-108">EXAMPLES</span></span>

### <span data-ttu-id="9fa45-109">1. példa: felhasználó munkamenetének leválasztása</span><span class="sxs-lookup"><span data-stu-id="9fa45-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="9fa45-110">Ez a parancs leválasztja az Azure RemoteApp-munkamenetet az ContosoApps-gyűjteményben annak a felhasználónak, akinek az UPN-je PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="9fa45-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="9fa45-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fa45-111">PARAMETERS</span></span>

### <span data-ttu-id="9fa45-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9fa45-112">-CollectionName</span></span>
<span data-ttu-id="9fa45-113">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fa45-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa45-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="9fa45-114">-Profile</span></span>
<span data-ttu-id="9fa45-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9fa45-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9fa45-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9fa45-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9fa45-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="9fa45-117">-UserUpn</span></span>
<span data-ttu-id="9fa45-118">Egy felhasználó egyszerű felhasználónevét adja meg PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="9fa45-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa45-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa45-119">CommonParameters</span></span>
<span data-ttu-id="9fa45-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fa45-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa45-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa45-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa45-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa45-122">INPUTS</span></span>

## <span data-ttu-id="9fa45-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa45-123">OUTPUTS</span></span>

## <span data-ttu-id="9fa45-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fa45-124">NOTES</span></span>

## <span data-ttu-id="9fa45-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fa45-125">RELATED LINKS</span></span>

[<span data-ttu-id="9fa45-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="9fa45-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="9fa45-127">Meghívó-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="9fa45-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="9fa45-128">Küldés-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="9fa45-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


