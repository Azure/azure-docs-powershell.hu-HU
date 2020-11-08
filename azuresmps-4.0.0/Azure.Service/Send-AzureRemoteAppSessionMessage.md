---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016433"
---
# <span data-ttu-id="33909-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="33909-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="33909-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33909-102">SYNOPSIS</span></span>
<span data-ttu-id="33909-103">Üzenetet küld egy felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="33909-103">Sends a message to a user.</span></span>

## <span data-ttu-id="33909-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33909-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33909-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33909-105">DESCRIPTION</span></span>
<span data-ttu-id="33909-106">A **Send-AzureRemoteAppSessionMessage** parancsmag üzenetet küld azoknak a felhasználóknak, akik Azure RemoteApp-munkamenethez csatlakoznak.</span><span class="sxs-lookup"><span data-stu-id="33909-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="33909-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33909-107">EXAMPLES</span></span>

### <span data-ttu-id="33909-108">1. példa: üzenet küldése egy felhasználónak</span><span class="sxs-lookup"><span data-stu-id="33909-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="33909-109">Ez a parancs üzenetet küld annak a felhasználónak, akinek az UPN-je PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="33909-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="33909-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33909-110">PARAMETERS</span></span>

### <span data-ttu-id="33909-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="33909-111">-CollectionName</span></span>
<span data-ttu-id="33909-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33909-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="33909-113">-Üzenet</span><span class="sxs-lookup"><span data-stu-id="33909-113">-Message</span></span>
<span data-ttu-id="33909-114">A küldendő üzenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="33909-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33909-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="33909-115">-Profile</span></span>
<span data-ttu-id="33909-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="33909-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33909-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="33909-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33909-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="33909-118">-UserUpn</span></span>
<span data-ttu-id="33909-119">Egy felhasználó egyszerű felhasználónevét adja meg, például PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="33909-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="33909-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33909-120">CommonParameters</span></span>
<span data-ttu-id="33909-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33909-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33909-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33909-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33909-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33909-123">INPUTS</span></span>

## <span data-ttu-id="33909-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33909-124">OUTPUTS</span></span>

## <span data-ttu-id="33909-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33909-125">NOTES</span></span>

## <span data-ttu-id="33909-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33909-126">RELATED LINKS</span></span>

[<span data-ttu-id="33909-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="33909-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="33909-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="33909-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="33909-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="33909-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


