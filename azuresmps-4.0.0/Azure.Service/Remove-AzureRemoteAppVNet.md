---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016146"
---
# <span data-ttu-id="be16a-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="be16a-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="be16a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be16a-102">SYNOPSIS</span></span>
<span data-ttu-id="be16a-103">Azure RemoteApp virtuális hálózat törlése</span><span class="sxs-lookup"><span data-stu-id="be16a-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="be16a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be16a-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="be16a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be16a-105">DESCRIPTION</span></span>
<span data-ttu-id="be16a-106">A **Remove-AzureRemoteAppVNet** parancsmag törli az Azure RemoteApp virtuális hálózatát.</span><span class="sxs-lookup"><span data-stu-id="be16a-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="be16a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be16a-107">EXAMPLES</span></span>

### <span data-ttu-id="be16a-108">Példa 1: meghatározott virtuális hálózat törlése</span><span class="sxs-lookup"><span data-stu-id="be16a-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="be16a-109">Ez a parancs törli a ContosoVNet nevű virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="be16a-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="be16a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be16a-110">PARAMETERS</span></span>

### <span data-ttu-id="be16a-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="be16a-111">-Profile</span></span>
<span data-ttu-id="be16a-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="be16a-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be16a-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="be16a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be16a-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="be16a-114">-VNetName</span></span>
<span data-ttu-id="be16a-115">A törlendő Azure RemoteApp virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be16a-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be16a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be16a-116">CommonParameters</span></span>
<span data-ttu-id="be16a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be16a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be16a-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be16a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be16a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be16a-119">INPUTS</span></span>

## <span data-ttu-id="be16a-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be16a-120">OUTPUTS</span></span>

## <span data-ttu-id="be16a-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be16a-121">NOTES</span></span>

## <span data-ttu-id="be16a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be16a-122">RELATED LINKS</span></span>

[<span data-ttu-id="be16a-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="be16a-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="be16a-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="be16a-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


