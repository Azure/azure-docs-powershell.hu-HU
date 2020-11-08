---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016015"
---
# <span data-ttu-id="849ef-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="849ef-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="849ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="849ef-102">SYNOPSIS</span></span>
<span data-ttu-id="849ef-103">A védelmi entitások tulajdonságait frissíti az Azure webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="849ef-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="849ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="849ef-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="849ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="849ef-105">DESCRIPTION</span></span>
<span data-ttu-id="849ef-106">Az **Update-AzureSiteRecoveryProtectionEntity** parancsmag az Azure webhely-helyreállításban (például a virtuális gép tulajdonosának adatai) frissíti a védelmi entitások tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="849ef-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="849ef-107">Ezt a parancsmagot csak a Virtual Machine monitor (VMM) támogatja, hogy VMM a védett védelmi entitásokat.</span><span class="sxs-lookup"><span data-stu-id="849ef-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="849ef-108">Példák</span><span class="sxs-lookup"><span data-stu-id="849ef-108">EXAMPLES</span></span>

### <span data-ttu-id="849ef-109">Példa 1: védelmi entitás frissítése</span><span class="sxs-lookup"><span data-stu-id="849ef-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="849ef-110">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védett tárolót, majd az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="849ef-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="849ef-111">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Container tárolt tárolóhoz tartozó védett virtuális gépet kapja, majd a $ProtectionEntity változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="849ef-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="849ef-112">A végleges parancs frissíti a védelmi entitást a $ProtectionEntityban.</span><span class="sxs-lookup"><span data-stu-id="849ef-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="849ef-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="849ef-113">PARAMETERS</span></span>

### <span data-ttu-id="849ef-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="849ef-114">-Profile</span></span>
<span data-ttu-id="849ef-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="849ef-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="849ef-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="849ef-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="849ef-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="849ef-117">-ProtectionEntity</span></span>
<span data-ttu-id="849ef-118">A frissítendő védelmi entitást adja meg.</span><span class="sxs-lookup"><span data-stu-id="849ef-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="849ef-119">Ha **ASRProtectionEntity** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryProtectionEntity** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="849ef-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="849ef-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="849ef-120">-WaitForCompletion</span></span>
<span data-ttu-id="849ef-121">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="849ef-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="849ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849ef-122">CommonParameters</span></span>
<span data-ttu-id="849ef-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="849ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849ef-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849ef-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="849ef-125">INPUTS</span></span>

## <span data-ttu-id="849ef-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="849ef-126">OUTPUTS</span></span>

## <span data-ttu-id="849ef-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="849ef-127">NOTES</span></span>

## <span data-ttu-id="849ef-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="849ef-128">RELATED LINKS</span></span>

[<span data-ttu-id="849ef-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="849ef-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="849ef-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="849ef-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="849ef-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="849ef-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


