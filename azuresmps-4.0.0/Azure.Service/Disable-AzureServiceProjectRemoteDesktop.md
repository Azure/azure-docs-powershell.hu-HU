---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015696"
---
# <span data-ttu-id="f6cc8-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f6cc8-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="f6cc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cc8-103">Letiltja a távoli asztali hozzáférést egy felhőalapú szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="f6cc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6cc8-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6cc8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="f6cc8-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f6cc8-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f6cc8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f6cc8-108">A **disable-AzureServiceProjectRemoteDesktop** letiltja a távoli asztali hozzáférést egy hosztolt szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="f6cc8-109">A módosítás érvénybe léptetéséhez a távoli asztali hozzáférés letiltása után közzé kell tennie a szolgáltatást a **Közzététel – AzureServiceProject** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="f6cc8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f6cc8-110">EXAMPLES</span></span>

## <span data-ttu-id="f6cc8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6cc8-111">PARAMETERS</span></span>

### <span data-ttu-id="f6cc8-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6cc8-112">-PassThru</span></span>
<span data-ttu-id="f6cc8-113">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6cc8-114">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cc8-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6cc8-115">-Profile</span></span>
<span data-ttu-id="f6cc8-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6cc8-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f6cc8-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6cc8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cc8-118">CommonParameters</span></span>
<span data-ttu-id="f6cc8-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6cc8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cc8-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6cc8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cc8-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6cc8-121">INPUTS</span></span>

## <span data-ttu-id="f6cc8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6cc8-122">OUTPUTS</span></span>

## <span data-ttu-id="f6cc8-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6cc8-123">NOTES</span></span>

## <span data-ttu-id="f6cc8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6cc8-124">RELATED LINKS</span></span>

[<span data-ttu-id="f6cc8-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f6cc8-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


