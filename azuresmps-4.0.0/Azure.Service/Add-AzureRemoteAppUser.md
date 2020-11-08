---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016381"
---
# <span data-ttu-id="cb83d-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="cb83d-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="cb83d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb83d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb83d-103">Hozzáad egy felhasználót egy Azure RemoteApp-gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="cb83d-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="cb83d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb83d-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb83d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb83d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb83d-106">Az **Add-AzureRemoteAppUser** parancsmag hozzáadja a felhasználót egy Azure RemoteApp-gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="cb83d-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="cb83d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cb83d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb83d-108">1. példa: felhasználó felvétele Microsoft-fiók használatával</span><span class="sxs-lookup"><span data-stu-id="cb83d-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="cb83d-109">Ez a parancs hozzáadja a Microsoft PattiFuller@contoso.com -fiókot a contoso nevű gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="cb83d-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="cb83d-110">2. példa: felhasználó hozzáadása Azure Active Directory-fiókkal</span><span class="sxs-lookup"><span data-stu-id="cb83d-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="cb83d-111">Ez a parancs hozzáadja az Azure Active Directory PattiFuller@contoso.com -fiókot a contoso nevű gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="cb83d-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="cb83d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb83d-112">PARAMETERS</span></span>

### <span data-ttu-id="cb83d-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="cb83d-113">-Alias</span></span>
<span data-ttu-id="cb83d-114">Egy közzétett program-aliast ad meg.</span><span class="sxs-lookup"><span data-stu-id="cb83d-114">Specifies a published program alias.</span></span>
<span data-ttu-id="cb83d-115">Ezt a paramétert csak a per-app közzétételi módjában tudja használni.</span><span class="sxs-lookup"><span data-stu-id="cb83d-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="cb83d-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="cb83d-116">-CollectionName</span></span>
<span data-ttu-id="cb83d-117">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb83d-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="cb83d-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb83d-118">-Profile</span></span>
<span data-ttu-id="cb83d-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cb83d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb83d-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cb83d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb83d-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="cb83d-121">-Type</span></span>
<span data-ttu-id="cb83d-122">A felhasználó típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb83d-122">Specifies a user type.</span></span>
<span data-ttu-id="cb83d-123">A paraméter elfogadható értékei a következők: OrgId vagy MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="cb83d-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="cb83d-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="cb83d-124">-UserUpn</span></span>
<span data-ttu-id="cb83d-125">Egy felhasználó egyszerű felhasználónevét adja meg, például PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="cb83d-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="cb83d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb83d-126">CommonParameters</span></span>
<span data-ttu-id="cb83d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb83d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb83d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb83d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb83d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb83d-129">INPUTS</span></span>

## <span data-ttu-id="cb83d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb83d-130">OUTPUTS</span></span>

## <span data-ttu-id="cb83d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb83d-131">NOTES</span></span>

## <span data-ttu-id="cb83d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb83d-132">RELATED LINKS</span></span>

[<span data-ttu-id="cb83d-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="cb83d-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="cb83d-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="cb83d-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


