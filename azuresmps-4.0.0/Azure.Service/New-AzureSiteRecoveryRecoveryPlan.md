---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015976"
---
# <span data-ttu-id="4431f-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4431f-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4431f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4431f-102">SYNOPSIS</span></span>
<span data-ttu-id="4431f-103">Webhely-helyreállítási csomagot hoz létre a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4431f-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="4431f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4431f-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4431f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4431f-105">DESCRIPTION</span></span>
<span data-ttu-id="4431f-106">A **New-AzureSiteRecoveryRecoveryPlan** parancsmag létrehoz egy helyreállítási tervet az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="4431f-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="4431f-107">A helyreállítási terv a virtuális gépeket egy csoportba gyűjti a feladatátvétel és helyreállítás céljából.</span><span class="sxs-lookup"><span data-stu-id="4431f-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="4431f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4431f-108">EXAMPLES</span></span>

### <span data-ttu-id="4431f-109">1. példa: helyreállítási terv hozzáadása a webhely-helyreállítási boltozathoz</span><span class="sxs-lookup"><span data-stu-id="4431f-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="4431f-110">Ez a parancs hozzáadja a RecoveryPlan.xml nevű helyreállítási csomagot az Azure-webhely helyreállítási boltozatához.</span><span class="sxs-lookup"><span data-stu-id="4431f-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4431f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4431f-111">PARAMETERS</span></span>

### <span data-ttu-id="4431f-112">-Fájl</span><span class="sxs-lookup"><span data-stu-id="4431f-112">-File</span></span>
<span data-ttu-id="4431f-113">A helyreállítási terv fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4431f-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="4431f-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="4431f-114">-Profile</span></span>
<span data-ttu-id="4431f-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4431f-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4431f-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4431f-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4431f-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4431f-117">-WaitForCompletion</span></span>
<span data-ttu-id="4431f-118">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="4431f-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="4431f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4431f-119">CommonParameters</span></span>
<span data-ttu-id="4431f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4431f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4431f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4431f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4431f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4431f-122">INPUTS</span></span>

## <span data-ttu-id="4431f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4431f-123">OUTPUTS</span></span>

## <span data-ttu-id="4431f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4431f-124">NOTES</span></span>

## <span data-ttu-id="4431f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4431f-125">RELATED LINKS</span></span>

[<span data-ttu-id="4431f-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4431f-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4431f-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4431f-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4431f-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4431f-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


