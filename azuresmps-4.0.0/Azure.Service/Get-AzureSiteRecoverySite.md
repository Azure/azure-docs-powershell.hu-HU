---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015577"
---
# <span data-ttu-id="16352-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="16352-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="16352-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16352-102">SYNOPSIS</span></span>
<span data-ttu-id="16352-103">Beilleszti a Hyper-V-webhelyeket egy webhely-helyreállítási Vault-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="16352-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="16352-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16352-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="16352-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16352-105">DESCRIPTION</span></span>
<span data-ttu-id="16352-106">A **Get-AzureSiteRecoverySite** parancsmag a Hyper-V-webhelyeket egy Azure-webhely helyreállítási pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="16352-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="16352-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16352-107">EXAMPLES</span></span>

### <span data-ttu-id="16352-108">1. példa: helyreállítási webhelyek beszerzése</span><span class="sxs-lookup"><span data-stu-id="16352-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="16352-109">Ez a parancs az aktuális boltozat helyreállítási webhelyeit kapja.</span><span class="sxs-lookup"><span data-stu-id="16352-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="16352-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16352-110">PARAMETERS</span></span>

### <span data-ttu-id="16352-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="16352-111">-Profile</span></span>
<span data-ttu-id="16352-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="16352-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16352-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="16352-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16352-114">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="16352-114">-Vault</span></span>
<span data-ttu-id="16352-115">A webhelyek beolvasására szolgáló boltozatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="16352-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="16352-116">Ha **ASRVault** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryVault** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="16352-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16352-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16352-117">CommonParameters</span></span>
<span data-ttu-id="16352-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16352-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16352-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16352-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16352-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16352-120">INPUTS</span></span>

## <span data-ttu-id="16352-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16352-121">OUTPUTS</span></span>

## <span data-ttu-id="16352-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16352-122">NOTES</span></span>

## <span data-ttu-id="16352-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16352-123">RELATED LINKS</span></span>

[<span data-ttu-id="16352-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="16352-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="16352-125">Új – AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="16352-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


