---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016149"
---
# <span data-ttu-id="1d9db-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1d9db-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="1d9db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d9db-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9db-103">Azure RemoteApp-sablon törlése</span><span class="sxs-lookup"><span data-stu-id="1d9db-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="1d9db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d9db-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d9db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d9db-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9db-106">A **Remove-AzureRemoteAppTemplateImage** parancsmag az Azure RemoteApp-sablon képét törli.</span><span class="sxs-lookup"><span data-stu-id="1d9db-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="1d9db-107">A sablonok képe csak akkor törölhető, ha az nem egy Azure RemoteApp-gyűjteményhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="1d9db-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1d9db-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1d9db-108">EXAMPLES</span></span>

### <span data-ttu-id="1d9db-109">Példa 1: sablon törlése kép</span><span class="sxs-lookup"><span data-stu-id="1d9db-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="1d9db-110">Ez a parancs törli a ContosoApps nevű sablon képét.</span><span class="sxs-lookup"><span data-stu-id="1d9db-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="1d9db-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d9db-111">PARAMETERS</span></span>

### <span data-ttu-id="1d9db-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1d9db-112">-ImageName</span></span>
<span data-ttu-id="1d9db-113">A RemoteApp-sablon képének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d9db-113">Specifies the name of the RemoteApp template image.</span></span>

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

### <span data-ttu-id="1d9db-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="1d9db-114">-Profile</span></span>
<span data-ttu-id="1d9db-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1d9db-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d9db-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1d9db-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d9db-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d9db-117">-Confirm</span></span>
<span data-ttu-id="1d9db-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d9db-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d9db-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d9db-119">-WhatIf</span></span>
<span data-ttu-id="1d9db-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d9db-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d9db-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d9db-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d9db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9db-122">CommonParameters</span></span>
<span data-ttu-id="1d9db-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d9db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9db-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9db-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9db-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d9db-125">INPUTS</span></span>

## <span data-ttu-id="1d9db-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d9db-126">OUTPUTS</span></span>

## <span data-ttu-id="1d9db-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d9db-127">NOTES</span></span>

## <span data-ttu-id="1d9db-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d9db-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d9db-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1d9db-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1d9db-130">Új – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1d9db-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1d9db-131">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1d9db-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


