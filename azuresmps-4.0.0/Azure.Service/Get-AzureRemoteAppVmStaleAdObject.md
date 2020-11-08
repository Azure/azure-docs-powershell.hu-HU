---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015630"
---
# <span data-ttu-id="50b13-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="50b13-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="50b13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50b13-102">SYNOPSIS</span></span>
<span data-ttu-id="50b13-103">Az Azure Active Directory olyan objektumait kapja, amelyek már nem léteznek az Azure RemoteApp virtuális gépekkel társítva.</span><span class="sxs-lookup"><span data-stu-id="50b13-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="50b13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50b13-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50b13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50b13-105">DESCRIPTION</span></span>
<span data-ttu-id="50b13-106">A **Get-AzureRemoteAppVmStaleAdObject** parancsmag az Azure Active Directory olyan objektumait kapja, amelyek már nem léteznek az Azure RemoteApp virtuális gépekhez társítva.</span><span class="sxs-lookup"><span data-stu-id="50b13-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="50b13-107">Ez a parancsmag a kapott objektumok nevét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="50b13-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="50b13-108">Példák</span><span class="sxs-lookup"><span data-stu-id="50b13-108">EXAMPLES</span></span>

### <span data-ttu-id="50b13-109">Példa 1: régi objektumok beszerzése gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="50b13-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="50b13-110">Ez a második parancs a contoso nevű gyűjtemény elavult objektumait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="50b13-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="50b13-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50b13-111">PARAMETERS</span></span>

### <span data-ttu-id="50b13-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="50b13-112">-CollectionName</span></span>
<span data-ttu-id="50b13-113">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50b13-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="50b13-114">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="50b13-114">-Credential</span></span>
<span data-ttu-id="50b13-115">A művelet végrehajtásához szükséges jogosultságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="50b13-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="50b13-116">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="50b13-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="50b13-117">Ha nem adja meg ezt a paramétert, ez a parancsmag az aktuális felhasználó hitelesítő adatait használja.</span><span class="sxs-lookup"><span data-stu-id="50b13-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="50b13-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="50b13-118">-Profile</span></span>
<span data-ttu-id="50b13-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="50b13-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50b13-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="50b13-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b13-121">CommonParameters</span></span>
<span data-ttu-id="50b13-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b13-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b13-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50b13-124">INPUTS</span></span>

## <span data-ttu-id="50b13-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50b13-125">OUTPUTS</span></span>

### <span data-ttu-id="50b13-126">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="50b13-126">String</span></span>

## <span data-ttu-id="50b13-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50b13-127">NOTES</span></span>

## <span data-ttu-id="50b13-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50b13-128">RELATED LINKS</span></span>

[<span data-ttu-id="50b13-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="50b13-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


