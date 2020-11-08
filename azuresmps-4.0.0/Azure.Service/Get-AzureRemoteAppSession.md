---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016577"
---
# <span data-ttu-id="e900d-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="e900d-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="e900d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e900d-102">SYNOPSIS</span></span>
<span data-ttu-id="e900d-103">Az összes aktív és leválasztott Azure RemoteApp-munkamenet listázása egy gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="e900d-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="e900d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e900d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e900d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e900d-105">DESCRIPTION</span></span>
<span data-ttu-id="e900d-106">A **Get-AzureRemoteAppSession** parancsmag az aktív és a kapcsolat nélküli Azure RemoteApp-munkamenetek listáját jeleníti meg egy Azure RemoteApp-gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="e900d-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e900d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e900d-107">EXAMPLES</span></span>

### <span data-ttu-id="e900d-108">Példa 1: egy gyűjtemény összes munkamenetének listázása</span><span class="sxs-lookup"><span data-stu-id="e900d-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="e900d-109">Ez a parancs felsorolja az Azure RemoteApp-gyűjtemény ContosoApps nevű összes munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="e900d-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="e900d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e900d-110">PARAMETERS</span></span>

### <span data-ttu-id="e900d-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e900d-111">-CollectionName</span></span>
<span data-ttu-id="e900d-112">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e900d-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="e900d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="e900d-113">-Profile</span></span>
<span data-ttu-id="e900d-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e900d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e900d-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e900d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e900d-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e900d-116">-UserUpn</span></span>
<span data-ttu-id="e900d-117">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az Azure RemoteApp-munkameneteket be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="e900d-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="e900d-118">Az egyszerű felhasználónév például a következő formátumú lehet: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="e900d-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="e900d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e900d-119">CommonParameters</span></span>
<span data-ttu-id="e900d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e900d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e900d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e900d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e900d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e900d-122">INPUTS</span></span>

## <span data-ttu-id="e900d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e900d-123">OUTPUTS</span></span>

## <span data-ttu-id="e900d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e900d-124">NOTES</span></span>

## <span data-ttu-id="e900d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e900d-125">RELATED LINKS</span></span>

[<span data-ttu-id="e900d-126">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="e900d-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="e900d-127">Meghívó-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="e900d-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="e900d-128">Küldés-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="e900d-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


