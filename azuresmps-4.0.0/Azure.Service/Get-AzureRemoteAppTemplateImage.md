---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016579"
---
# <span data-ttu-id="8f5d4-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8f5d4-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="8f5d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5d4-103">Információt keres az Azure RemoteApp-sablon képeiről.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="8f5d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f5d4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f5d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5d4-106">A **Get-AzureRemoteAppTemplateImage** parancsmag információkat keres az Azure RemoteApp-sablon képeiről a Microsoft Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="8f5d4-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely a megadott sablon képével kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="8f5d4-108">Ha nincs megadva sablon képe, az aktuális előfizetésben lévő összes sablon képéről információt olvas be.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="8f5d4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f5d4-109">EXAMPLES</span></span>

### <span data-ttu-id="8f5d4-110">Példa 1: az összes sablonból álló képek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="8f5d4-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="8f5d4-111">Ez a parancs megjeleníti az összes sablon képeinek listáját.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="8f5d4-112">2. példa: adatok beolvasása egy adott sablonról</span><span class="sxs-lookup"><span data-stu-id="8f5d4-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="8f5d4-113">Ez a parancs információkat olvas be a ContosoApps nevű sablon képéről.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="8f5d4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f5d4-114">PARAMETERS</span></span>

### <span data-ttu-id="8f5d4-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8f5d4-115">-ImageName</span></span>
<span data-ttu-id="8f5d4-116">Egy Azure RemoteApp-sablon nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="8f5d4-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8f5d4-117">-Profile</span></span>
<span data-ttu-id="8f5d4-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f5d4-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8f5d4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f5d4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5d4-120">CommonParameters</span></span>
<span data-ttu-id="8f5d4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f5d4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5d4-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5d4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5d4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5d4-123">INPUTS</span></span>

## <span data-ttu-id="8f5d4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5d4-124">OUTPUTS</span></span>

## <span data-ttu-id="8f5d4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f5d4-125">NOTES</span></span>

## <span data-ttu-id="8f5d4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f5d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f5d4-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8f5d4-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="8f5d4-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="8f5d4-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


