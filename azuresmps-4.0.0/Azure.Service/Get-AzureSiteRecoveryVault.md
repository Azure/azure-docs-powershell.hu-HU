---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016565"
---
# <span data-ttu-id="647a1-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="647a1-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="647a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="647a1-102">SYNOPSIS</span></span>
<span data-ttu-id="647a1-103">Webhely-helyreállítási boltozatokat kap a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="647a1-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="647a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="647a1-104">SYNTAX</span></span>

### <span data-ttu-id="647a1-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="647a1-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="647a1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="647a1-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="647a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="647a1-107">DESCRIPTION</span></span>
<span data-ttu-id="647a1-108">A **Get-AzureSiteRecoveryVault** parancsmag a jelenlegi előfizetésből kapja meg az Azure webhelyek helyreállítási boltozatai vagy egy bizonyos webhely-helyreállítási tároló listáját.</span><span class="sxs-lookup"><span data-stu-id="647a1-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="647a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="647a1-109">EXAMPLES</span></span>

### <span data-ttu-id="647a1-110">1. példa: az aktív boltozat beolvasása</span><span class="sxs-lookup"><span data-stu-id="647a1-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="647a1-111">Ez a parancs beolvassa az aktív Azure webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="647a1-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="647a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="647a1-112">PARAMETERS</span></span>

### <span data-ttu-id="647a1-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="647a1-113">-Name</span></span>
<span data-ttu-id="647a1-114">A beolvasott pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="647a1-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647a1-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="647a1-115">-Profile</span></span>
<span data-ttu-id="647a1-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="647a1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="647a1-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="647a1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="647a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647a1-118">CommonParameters</span></span>
<span data-ttu-id="647a1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="647a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647a1-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647a1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="647a1-121">INPUTS</span></span>

## <span data-ttu-id="647a1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="647a1-122">OUTPUTS</span></span>

## <span data-ttu-id="647a1-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="647a1-123">NOTES</span></span>

## <span data-ttu-id="647a1-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="647a1-124">RELATED LINKS</span></span>

[<span data-ttu-id="647a1-125">Új – AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="647a1-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


