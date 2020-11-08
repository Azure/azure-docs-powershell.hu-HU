---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015892"
---
# <span data-ttu-id="39d49-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="39d49-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="39d49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39d49-102">SYNOPSIS</span></span>
<span data-ttu-id="39d49-103">Webhely-helyreállítási webhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="39d49-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="39d49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39d49-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39d49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39d49-105">DESCRIPTION</span></span>
<span data-ttu-id="39d49-106">A **New-AzureSiteRecoverySite** parancsmag létrehoz egy Azure webhely-helyreállítási webhelyet az aktuális boltívben.</span><span class="sxs-lookup"><span data-stu-id="39d49-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="39d49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39d49-107">EXAMPLES</span></span>

### <span data-ttu-id="39d49-108">1. példa: webhely-helyreállítási webhely létrehozása</span><span class="sxs-lookup"><span data-stu-id="39d49-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="39d49-109">Ez a parancs létrehoz egy RecoverySite07 nevű webhely-helyreállítási webhelyet.</span><span class="sxs-lookup"><span data-stu-id="39d49-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="39d49-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39d49-110">PARAMETERS</span></span>

### <span data-ttu-id="39d49-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39d49-111">-Name</span></span>
<span data-ttu-id="39d49-112">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39d49-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d49-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="39d49-113">-Profile</span></span>
<span data-ttu-id="39d49-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="39d49-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39d49-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="39d49-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39d49-116">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="39d49-116">-Vault</span></span>
<span data-ttu-id="39d49-117">Azt a boltozatot adja meg, amelybe a webhelyet létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="39d49-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="39d49-118">Ha **ASRVault** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryVault** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="39d49-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="39d49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d49-119">CommonParameters</span></span>
<span data-ttu-id="39d49-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39d49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d49-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d49-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d49-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d49-122">INPUTS</span></span>

## <span data-ttu-id="39d49-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d49-123">OUTPUTS</span></span>

## <span data-ttu-id="39d49-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39d49-124">NOTES</span></span>

## <span data-ttu-id="39d49-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39d49-125">RELATED LINKS</span></span>

[<span data-ttu-id="39d49-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="39d49-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="39d49-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="39d49-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


