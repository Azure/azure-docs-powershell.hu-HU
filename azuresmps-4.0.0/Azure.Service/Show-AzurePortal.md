---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015948"
---
# <span data-ttu-id="ca79d-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="ca79d-101">Show-AzurePortal</span></span>

## <span data-ttu-id="ca79d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca79d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca79d-103">Az Azure felügyeleti portál megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="ca79d-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="ca79d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca79d-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca79d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca79d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca79d-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ca79d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ca79d-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ca79d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ca79d-108">A **show-AzurePortal** parancsmag az Azure felügyeleti portált jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ca79d-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="ca79d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ca79d-109">EXAMPLES</span></span>

### <span data-ttu-id="ca79d-110">1. példa: webhely adatainak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="ca79d-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="ca79d-111">Ez a példa az Azure portálon megnyit egy böngészőt, amely a mySite nevű webhelyre vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ca79d-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="ca79d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca79d-112">PARAMETERS</span></span>

### <span data-ttu-id="ca79d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ca79d-113">-Environment</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca79d-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca79d-114">-Name</span></span>
<span data-ttu-id="ca79d-115">Annak a webhelynek a neve, amelyet meg szeretne jeleníteni a portálon.</span><span class="sxs-lookup"><span data-stu-id="ca79d-115">Specifies the name of the website to show in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca79d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="ca79d-116">-Profile</span></span>
<span data-ttu-id="ca79d-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ca79d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca79d-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ca79d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca79d-119">-Realm</span><span class="sxs-lookup"><span data-stu-id="ca79d-119">-Realm</span></span>
<span data-ttu-id="ca79d-120">Az Azure-portál megjelenítésekor az összevont hitelesítéshez használandó szervezeti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca79d-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca79d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca79d-121">CommonParameters</span></span>
<span data-ttu-id="ca79d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca79d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca79d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca79d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca79d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca79d-124">INPUTS</span></span>

## <span data-ttu-id="ca79d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca79d-125">OUTPUTS</span></span>

## <span data-ttu-id="ca79d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca79d-126">NOTES</span></span>

## <span data-ttu-id="ca79d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca79d-127">RELATED LINKS</span></span>

[<span data-ttu-id="ca79d-128">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca79d-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


