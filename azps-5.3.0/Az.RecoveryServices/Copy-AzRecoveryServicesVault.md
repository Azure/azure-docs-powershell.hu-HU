---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466662"
---
# <span data-ttu-id="87a2b-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="87a2b-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="87a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="87a2b-103">Adatokat másol egy tárolóból az egyik régióból egy másik régió egyik tárolójába.</span><span class="sxs-lookup"><span data-stu-id="87a2b-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="87a2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87a2b-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="87a2b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="87a2b-106">A **Copy-AzRecoveryServicesVault** parancsmag az egyik régió egyik tárolója adatait egy másik régió tárolójára másolja.</span><span class="sxs-lookup"><span data-stu-id="87a2b-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="87a2b-107">Jelenleg csak a tárolószintű adatok áthelyezését támogatjuk.</span><span class="sxs-lookup"><span data-stu-id="87a2b-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="87a2b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87a2b-108">EXAMPLES</span></span>

### <span data-ttu-id="87a2b-109">1. példa: Adatok másolása a tárolóból a tároló2-be</span><span class="sxs-lookup"><span data-stu-id="87a2b-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="87a2b-110">Az első két parancsmag lehívja a Recovery Services-tárolót – a tároló1 és a tároló2.</span><span class="sxs-lookup"><span data-stu-id="87a2b-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="87a2b-111">A második parancs elindítja a teljes adatátugrásokat a tároló1-ről a tároló2-re.</span><span class="sxs-lookup"><span data-stu-id="87a2b-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="87a2b-112">2. példa: Adatok másolása a tároló1-ból a tároló2-be csak sikertelen elemek esetén</span><span class="sxs-lookup"><span data-stu-id="87a2b-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="87a2b-113">Az első két parancsmag lehívja a Recovery Services-tárolót – a tároló1 és a tároló2.</span><span class="sxs-lookup"><span data-stu-id="87a2b-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="87a2b-114">A második parancs részleges adatátköltözéseket indít el a tároló1-ről a tároló2-re, csak azok az elemek esetén, amelyek a korábbi áthelyezési műveletek során sikertelenek.</span><span class="sxs-lookup"><span data-stu-id="87a2b-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="87a2b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a2b-115">PARAMETERS</span></span>

### <span data-ttu-id="87a2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a2b-116">-DefaultProfile</span></span>
<span data-ttu-id="87a2b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87a2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a2b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="87a2b-118">-Force</span></span>
<span data-ttu-id="87a2b-119">Kényszeríti az adatáthelyítési műveletet (megakadályozza a megerősítést kérő párbeszédpanelt) anélkül, hogy megerősítést kér a céltár tárolási redundanciának típusára.</span><span class="sxs-lookup"><span data-stu-id="87a2b-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="87a2b-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="87a2b-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="87a2b-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="87a2b-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="87a2b-122">A paraméter váltásával próbálja meg áthelyezni a forrástárolóban található olyan tárolók adatait, amelyek még nincsenek áthelyezve.</span><span class="sxs-lookup"><span data-stu-id="87a2b-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="87a2b-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="87a2b-123">-SourceVault</span></span>
<span data-ttu-id="87a2b-124">Az áthelyezni fog egy forrástár-objektumot.</span><span class="sxs-lookup"><span data-stu-id="87a2b-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a2b-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="87a2b-125">-TargetVault</span></span>
<span data-ttu-id="87a2b-126">A céltár objektuma, ahová az adatokat át kell áthelyezni.</span><span class="sxs-lookup"><span data-stu-id="87a2b-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a2b-127">CommonParameters</span></span>
<span data-ttu-id="87a2b-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a2b-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87a2b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a2b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87a2b-130">INPUTS</span></span>

### <span data-ttu-id="87a2b-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="87a2b-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="87a2b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87a2b-132">OUTPUTS</span></span>

### <span data-ttu-id="87a2b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="87a2b-133">System.String</span></span>

## <span data-ttu-id="87a2b-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87a2b-134">NOTES</span></span>

## <span data-ttu-id="87a2b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87a2b-135">RELATED LINKS</span></span>
