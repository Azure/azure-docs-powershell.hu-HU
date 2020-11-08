---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016566"
---
# <span data-ttu-id="80598-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="80598-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="80598-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80598-102">SYNOPSIS</span></span>
<span data-ttu-id="80598-103">A webhely-helyreállítási boltozat beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80598-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="80598-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80598-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80598-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80598-105">DESCRIPTION</span></span>
<span data-ttu-id="80598-106">A **Get-AzureSiteRecoveryVaultSettings** parancsmag a jelenlegi Azure-webhely helyreállítási boltozatához kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80598-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="80598-107">Példák</span><span class="sxs-lookup"><span data-stu-id="80598-107">EXAMPLES</span></span>

### <span data-ttu-id="80598-108">Példa 1: beállítási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="80598-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="80598-109">Ez a parancs a jelenlegi Azure webhely-helyreállítási boltozat beállításaival kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80598-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="80598-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80598-110">PARAMETERS</span></span>

### <span data-ttu-id="80598-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="80598-111">-Profile</span></span>
<span data-ttu-id="80598-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="80598-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80598-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="80598-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80598-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80598-114">CommonParameters</span></span>
<span data-ttu-id="80598-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80598-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80598-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80598-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80598-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80598-117">INPUTS</span></span>

## <span data-ttu-id="80598-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80598-118">OUTPUTS</span></span>

## <span data-ttu-id="80598-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80598-119">NOTES</span></span>

## <span data-ttu-id="80598-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80598-120">RELATED LINKS</span></span>

[<span data-ttu-id="80598-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="80598-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="80598-122">Importálás – AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="80598-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


