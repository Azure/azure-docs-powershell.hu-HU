---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015974"
---
# <span data-ttu-id="a53ab-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a53ab-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="a53ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a53ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a53ab-103">Webhely-helyreállítási szolgáltatások boltozatának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a53ab-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="a53ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a53ab-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a53ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a53ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a53ab-106">A **New-AzureSiteRecoveryVault** parancsmag létrehoz egy Azure site Recovery Services Vault-t.</span><span class="sxs-lookup"><span data-stu-id="a53ab-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="a53ab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a53ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a53ab-108">1. példa: boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a53ab-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="a53ab-109">Ez a parancs létrehoz egy ContosoVault nevű boltozatot a Nyugat-amerikai térségben.</span><span class="sxs-lookup"><span data-stu-id="a53ab-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="a53ab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a53ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a53ab-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="a53ab-111">-Location</span></span>
<span data-ttu-id="a53ab-112">A földrajzi helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a53ab-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="a53ab-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a53ab-113">-Name</span></span>
<span data-ttu-id="a53ab-114">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a53ab-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="a53ab-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a53ab-115">-Profile</span></span>
<span data-ttu-id="a53ab-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a53ab-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a53ab-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a53ab-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a53ab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53ab-118">CommonParameters</span></span>
<span data-ttu-id="a53ab-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a53ab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53ab-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53ab-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53ab-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a53ab-121">INPUTS</span></span>

## <span data-ttu-id="a53ab-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a53ab-122">OUTPUTS</span></span>

## <span data-ttu-id="a53ab-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a53ab-123">NOTES</span></span>

## <span data-ttu-id="a53ab-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a53ab-124">RELATED LINKS</span></span>

[<span data-ttu-id="a53ab-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a53ab-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


