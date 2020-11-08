---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015703"
---
# <span data-ttu-id="3697b-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="3697b-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="3697b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3697b-102">SYNOPSIS</span></span>
<span data-ttu-id="3697b-103">Eltávolítja az Azure Active Directory azon objektumait, amelyek már nem léteznek az Azure RemoteApp virtuális gépekhez társítottak.</span><span class="sxs-lookup"><span data-stu-id="3697b-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="3697b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3697b-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3697b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3697b-105">DESCRIPTION</span></span>
<span data-ttu-id="3697b-106">A **Clear-AzureRemoteAppVmStaleAdObject** parancsmag eltávolítja az Azure Active Directory azon objektumait, amelyek már nem léteznek az Azure RemoteApp virtuális gépekkel társítva.</span><span class="sxs-lookup"><span data-stu-id="3697b-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="3697b-107">Az Azure Active Directory-objektumok eltávolításához jogosultsággal rendelkező hitelesítő adatokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="3697b-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="3697b-108">Ha a *részletes* általános paramétert adja meg, ez a parancsmag a törölt objektumok nevét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3697b-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="3697b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3697b-109">EXAMPLES</span></span>

### <span data-ttu-id="3697b-110">1. példa: egy gyűjtemény elavult objektumainak törlése</span><span class="sxs-lookup"><span data-stu-id="3697b-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="3697b-111">Az első parancs a **beolvasás-hitelesítő adatok** használatával kéri a Felhasználónév és a jelszó megadását.</span><span class="sxs-lookup"><span data-stu-id="3697b-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="3697b-112">A parancs az eredményt a $AdminCredentials változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3697b-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="3697b-113">A második parancs törli a contoso nevű gyűjtemény régi objektumait.</span><span class="sxs-lookup"><span data-stu-id="3697b-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="3697b-114">A parancs a $AdminCredentials változóban tárolt hitelesítő adatokat használja.</span><span class="sxs-lookup"><span data-stu-id="3697b-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="3697b-115">Ahhoz, hogy a parancs sikeres legyen, a hitelesítő adatoknak megfelelő jogokkal kell rendelkezniük.</span><span class="sxs-lookup"><span data-stu-id="3697b-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="3697b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3697b-116">PARAMETERS</span></span>

### <span data-ttu-id="3697b-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3697b-117">-CollectionName</span></span>
<span data-ttu-id="3697b-118">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3697b-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3697b-119">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="3697b-119">-Credential</span></span>
<span data-ttu-id="3697b-120">A művelet végrehajtásához szükséges jogosultságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3697b-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="3697b-121">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3697b-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="3697b-122">Ha nem adja meg ezt a paramétert, ez a parancsmag az aktuális felhasználó hitelesítő adatait használja.</span><span class="sxs-lookup"><span data-stu-id="3697b-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3697b-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3697b-123">-Profile</span></span>
<span data-ttu-id="3697b-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3697b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3697b-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3697b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3697b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3697b-126">-Confirm</span></span>
<span data-ttu-id="3697b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3697b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3697b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3697b-128">-WhatIf</span></span>
<span data-ttu-id="3697b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3697b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3697b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3697b-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3697b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3697b-131">CommonParameters</span></span>
<span data-ttu-id="3697b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3697b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3697b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3697b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3697b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3697b-134">INPUTS</span></span>

## <span data-ttu-id="3697b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3697b-135">OUTPUTS</span></span>

## <span data-ttu-id="3697b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3697b-136">NOTES</span></span>

## <span data-ttu-id="3697b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3697b-137">RELATED LINKS</span></span>

[<span data-ttu-id="3697b-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="3697b-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


