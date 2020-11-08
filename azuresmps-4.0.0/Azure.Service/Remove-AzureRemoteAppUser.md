---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015866"
---
# <span data-ttu-id="dc13c-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dc13c-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="dc13c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc13c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc13c-103">Felhasználó eltávolítása Azure RemoteApp-gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="dc13c-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dc13c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc13c-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc13c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc13c-105">DESCRIPTION</span></span>
<span data-ttu-id="dc13c-106">A **Remove-AzureRemoteAppUser** parancsmag az Azure RemoteApp-gyűjteményből távolítja el a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="dc13c-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dc13c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc13c-107">EXAMPLES</span></span>

### <span data-ttu-id="dc13c-108">Example1: felhasználó eltávolítása egy gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="dc13c-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="dc13c-109">Ez a parancs eltávolítja az Azure ActiveDirectory felhasználót PattiFuller@contoso.com a contoso gyűjteményéből.</span><span class="sxs-lookup"><span data-stu-id="dc13c-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="dc13c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc13c-110">PARAMETERS</span></span>

### <span data-ttu-id="dc13c-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="dc13c-111">-Alias</span></span>
<span data-ttu-id="dc13c-112">Egy közzétett program-aliast ad meg.</span><span class="sxs-lookup"><span data-stu-id="dc13c-112">Specifies a published program alias.</span></span>
<span data-ttu-id="dc13c-113">Ezt a paramétert csak a per-app közzétételi módjában tudja használni.</span><span class="sxs-lookup"><span data-stu-id="dc13c-113">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc13c-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="dc13c-114">-CollectionName</span></span>
<span data-ttu-id="dc13c-115">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc13c-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="dc13c-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="dc13c-116">-Profile</span></span>
<span data-ttu-id="dc13c-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dc13c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc13c-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dc13c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc13c-119">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="dc13c-119">-Type</span></span>
<span data-ttu-id="dc13c-120">A felhasználó típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc13c-120">Specifies a user type.</span></span>
<span data-ttu-id="dc13c-121">A paraméter elfogadható értékei a következők: OrgId vagy MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="dc13c-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc13c-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="dc13c-122">-UserUpn</span></span>
<span data-ttu-id="dc13c-123">Egy felhasználó egyszerű felhasználónevét adja meg, például user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dc13c-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc13c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc13c-124">CommonParameters</span></span>
<span data-ttu-id="dc13c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc13c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc13c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc13c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc13c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc13c-127">INPUTS</span></span>

## <span data-ttu-id="dc13c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc13c-128">OUTPUTS</span></span>

## <span data-ttu-id="dc13c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc13c-129">NOTES</span></span>

## <span data-ttu-id="dc13c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc13c-130">RELATED LINKS</span></span>

[<span data-ttu-id="dc13c-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dc13c-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="dc13c-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dc13c-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


