---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 313E7444-2EB4-4B91-9E56-5730CB006046
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 5279ca9664c827bdb85b42519f6776c10ab37e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494633"
---
# <span data-ttu-id="b5ff6-101">Update-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b5ff6-101">Update-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="b5ff6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5ff6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ff6-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5ff6-103">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ff6-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5ff6-104">DESCRIPTION</span></span>

## <span data-ttu-id="b5ff6-105">Példák</span><span class="sxs-lookup"><span data-stu-id="b5ff6-105">EXAMPLES</span></span>

## <span data-ttu-id="b5ff6-106">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5ff6-106">PARAMETERS</span></span>

### <span data-ttu-id="b5ff6-107">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b5ff6-107">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-108">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="b5ff6-108">-Authentication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-109">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="b5ff6-109">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-110">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="b5ff6-110">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-111">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b5ff6-111">-Policy</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-112">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b5ff6-112">-RecoveryAzureStorageAccountId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-113">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="b5ff6-113">-RecoveryPoints</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-114">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b5ff6-114">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-115">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b5ff6-115">-ReplicationFrequencyInSeconds</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-116">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b5ff6-116">-ReplicationMethod</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-117">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b5ff6-117">-ReplicationPort</span></span>
```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-118">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b5ff6-118">-ReplicationStartTime</span></span>
```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ff6-119">-DefaultProfile</span></span>
<span data-ttu-id="b5ff6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5ff6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ff6-121">CommonParameters</span></span>
<span data-ttu-id="b5ff6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5ff6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ff6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ff6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ff6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ff6-124">INPUTS</span></span>

### <span data-ttu-id="b5ff6-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b5ff6-125">ASRPolicy</span></span>
<span data-ttu-id="b5ff6-126">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b5ff6-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b5ff6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ff6-127">OUTPUTS</span></span>

## <span data-ttu-id="b5ff6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5ff6-128">NOTES</span></span>

## <span data-ttu-id="b5ff6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5ff6-129">RELATED LINKS</span></span>

