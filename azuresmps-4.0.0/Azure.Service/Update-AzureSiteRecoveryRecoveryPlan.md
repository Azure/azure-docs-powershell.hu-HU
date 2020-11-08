---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016014"
---
# <span data-ttu-id="eb4c3-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb4c3-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="eb4c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4c3-103">Helyreállítási terv frissítése a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="eb4c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb4c3-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb4c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb4c3-105">DESCRIPTION</span></span>
<span data-ttu-id="eb4c3-106">Az **Update-AzureSiteRecoveryRecoveryPlan** parancsmag az Azure-webhely helyreállításakor frissíti a helyreállítási tervet, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="eb4c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb4c3-107">EXAMPLES</span></span>

### <span data-ttu-id="eb4c3-108">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="eb4c3-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="eb4c3-109">Ez a parancs frissíti a megadott helyreállítási csomagot, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="eb4c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb4c3-110">PARAMETERS</span></span>

### <span data-ttu-id="eb4c3-111">-Fájl</span><span class="sxs-lookup"><span data-stu-id="eb4c3-111">-File</span></span>
<span data-ttu-id="eb4c3-112">A parancsmag által frissített helyreállítási terv helyreállítási tervének fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="eb4c3-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb4c3-113">-Profile</span></span>
<span data-ttu-id="eb4c3-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb4c3-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb4c3-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="eb4c3-116">-WaitForCompletion</span></span>
<span data-ttu-id="eb4c3-117">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="eb4c3-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="eb4c3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4c3-118">CommonParameters</span></span>
<span data-ttu-id="eb4c3-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb4c3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4c3-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb4c3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4c3-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb4c3-121">INPUTS</span></span>

## <span data-ttu-id="eb4c3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb4c3-122">OUTPUTS</span></span>

## <span data-ttu-id="eb4c3-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb4c3-123">NOTES</span></span>

## <span data-ttu-id="eb4c3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb4c3-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb4c3-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb4c3-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="eb4c3-126">Új – AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb4c3-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="eb4c3-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="eb4c3-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


