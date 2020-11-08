---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015474"
---
# <span data-ttu-id="55d8b-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="55d8b-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="55d8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="55d8b-103">Az Azure RemoteApp-sablon képének átnevezése</span><span class="sxs-lookup"><span data-stu-id="55d8b-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="55d8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55d8b-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="55d8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="55d8b-106">Az **Rename-AzureRemoteAppTemplateImage** parancsmag az Azure RemoteApp-sablon képét átnevezi.</span><span class="sxs-lookup"><span data-stu-id="55d8b-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="55d8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="55d8b-108">Példa 1: sablon átnevezése kép</span><span class="sxs-lookup"><span data-stu-id="55d8b-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="55d8b-109">Ez a parancs átnevezi az Azure RemoteApp template nevű ContosoApps a ContosoFinanceApps nevű képet.</span><span class="sxs-lookup"><span data-stu-id="55d8b-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="55d8b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="55d8b-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="55d8b-111">-ImageName</span></span>
<span data-ttu-id="55d8b-112">Annak az Azure RemoteApp-sablonnak a neve, amelyet átnevezni szeretne.</span><span class="sxs-lookup"><span data-stu-id="55d8b-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55d8b-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="55d8b-113">-NewName</span></span>
<span data-ttu-id="55d8b-114">Új nevet ad az Azure RemoteApp-sablon képhez.</span><span class="sxs-lookup"><span data-stu-id="55d8b-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="55d8b-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="55d8b-115">-Profile</span></span>
<span data-ttu-id="55d8b-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="55d8b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="55d8b-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="55d8b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55d8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d8b-118">CommonParameters</span></span>
<span data-ttu-id="55d8b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55d8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d8b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d8b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d8b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55d8b-121">INPUTS</span></span>

## <span data-ttu-id="55d8b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55d8b-122">OUTPUTS</span></span>

## <span data-ttu-id="55d8b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55d8b-123">NOTES</span></span>

## <span data-ttu-id="55d8b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55d8b-124">RELATED LINKS</span></span>

[<span data-ttu-id="55d8b-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="55d8b-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="55d8b-126">Új – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="55d8b-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="55d8b-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="55d8b-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


