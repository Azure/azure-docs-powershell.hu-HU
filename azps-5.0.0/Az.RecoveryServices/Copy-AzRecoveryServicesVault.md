---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188221"
---
# <span data-ttu-id="ceecd-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ceecd-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ceecd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceecd-102">SYNOPSIS</span></span>
<span data-ttu-id="ceecd-103">Az egyik régióban lévő boltozatból másolhatja az adatot egy másik régióban lévő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="ceecd-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="ceecd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceecd-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="ceecd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceecd-105">DESCRIPTION</span></span>
<span data-ttu-id="ceecd-106">A **copy-AzRecoveryServicesVault** parancsmag az egyik régióban lévő boltozatból másol adatot egy másik régióban lévő boltozatra.</span><span class="sxs-lookup"><span data-stu-id="ceecd-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="ceecd-107">Jelenleg csak a Vault-szintű adatáthelyezést támogatjuk.</span><span class="sxs-lookup"><span data-stu-id="ceecd-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="ceecd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ceecd-108">EXAMPLES</span></span>

### <span data-ttu-id="ceecd-109">1. példa: az vault1-ról a vault2-ra másolt Adatmásolás</span><span class="sxs-lookup"><span data-stu-id="ceecd-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="ceecd-110">-Force</span><span class="sxs-lookup"><span data-stu-id="ceecd-110">-Force</span></span>
<span data-ttu-id="ceecd-111">Kényszeríti az adatáthelyezési műveletet (megakadályozza a megerősítési párbeszédpanelt) a TARGET Vault-tárterület-tárolási redundancia-típus megerősítésének kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ceecd-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="ceecd-112">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ceecd-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="ceecd-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="ceecd-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="ceecd-114">Váltás a paraméterre az adatáthelyezéshez csak a forrásban lévő tárolók esetében, amelyek még nincsenek áthelyezve.</span><span class="sxs-lookup"><span data-stu-id="ceecd-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="ceecd-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="ceecd-115">-SourceVault</span></span>
<span data-ttu-id="ceecd-116">Az áthelyezni kívánt forrásobjektum-objektum.</span><span class="sxs-lookup"><span data-stu-id="ceecd-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="ceecd-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="ceecd-117">-TargetVault</span></span>
<span data-ttu-id="ceecd-118">A cél boltozat objektum, amelybe az adatot át kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="ceecd-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="ceecd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceecd-119">CommonParameters</span></span>
<span data-ttu-id="ceecd-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceecd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceecd-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ceecd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceecd-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceecd-122">INPUTS</span></span>

### <span data-ttu-id="ceecd-123">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ceecd-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ceecd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceecd-124">OUTPUTS</span></span>

### <span data-ttu-id="ceecd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ceecd-125">System.String</span></span>

## <span data-ttu-id="ceecd-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceecd-126">NOTES</span></span>

## <span data-ttu-id="ceecd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceecd-127">RELATED LINKS</span></span>
