---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672510"
---
# <span data-ttu-id="ff5c7-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ff5c7-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="ff5c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5c7-103">Beállítja a webhely-helyreállítási védelem entitás állapotát.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff5c7-104">SYNTAX</span></span>

### <span data-ttu-id="ff5c7-105">Letiltó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff5c7-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5c7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ff5c7-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff5c7-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="ff5c7-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff5c7-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="ff5c7-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff5c7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff5c7-109">DESCRIPTION</span></span>
<span data-ttu-id="ff5c7-110">A **set-AzureRmSiteRecoveryProtectionEntity** parancsmag engedélyezi vagy letiltja a védelmet az Azure webhely-helyreállítási védelmi entitások számára.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="ff5c7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ff5c7-111">EXAMPLES</span></span>

## <span data-ttu-id="ff5c7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff5c7-112">PARAMETERS</span></span>

### <span data-ttu-id="ff5c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5c7-113">-DefaultProfile</span></span>
<span data-ttu-id="ff5c7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ff5c7-115">-Force</span></span>
<span data-ttu-id="ff5c7-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff5c7-117">-OS</span><span class="sxs-lookup"><span data-stu-id="ff5c7-117">-OS</span></span>
<span data-ttu-id="ff5c7-118">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-118">Specifies the operating system type.</span></span>
<span data-ttu-id="ff5c7-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ff5c7-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff5c7-120">Windows</span><span class="sxs-lookup"><span data-stu-id="ff5c7-120">Windows</span></span>
- <span data-ttu-id="ff5c7-121">Linux</span><span class="sxs-lookup"><span data-stu-id="ff5c7-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="ff5c7-122">-OSDiskName</span></span>
<span data-ttu-id="ff5c7-123">Az operációs rendszert tartalmazó lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-124">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ff5c7-124">-Policy</span></span>
<span data-ttu-id="ff5c7-125">A webhely-helyreállítási házirend objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-126">-Védelem</span><span class="sxs-lookup"><span data-stu-id="ff5c7-126">-Protection</span></span>
<span data-ttu-id="ff5c7-127">Megadja, hogy engedélyezve vagy le kell-e tiltani a védelmet.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="ff5c7-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ff5c7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff5c7-129">Engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ff5c7-129">Enable</span></span>
- <span data-ttu-id="ff5c7-130">Megbénít</span><span class="sxs-lookup"><span data-stu-id="ff5c7-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ff5c7-131">-ProtectionEntity</span></span>
<span data-ttu-id="ff5c7-132">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-132">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="ff5c7-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff5c7-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ff5c7-134">A cél Azure-tároló fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ff5c7-135">-WaitForCompletion</span></span>
<span data-ttu-id="ff5c7-136">Jelzi, hogy a parancs a visszatérés előtt várja a befejezést.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-136">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="ff5c7-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff5c7-137">-Confirm</span></span>
<span data-ttu-id="ff5c7-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5c7-139">-WhatIf</span></span>
<span data-ttu-id="ff5c7-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ff5c7-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff5c7-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5c7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5c7-142">CommonParameters</span></span>
<span data-ttu-id="ff5c7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff5c7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5c7-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5c7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5c7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5c7-145">INPUTS</span></span>

### <span data-ttu-id="ff5c7-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ff5c7-146">ASRProtectionEntity</span></span>
<span data-ttu-id="ff5c7-147">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ff5c7-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="ff5c7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5c7-148">OUTPUTS</span></span>

### <span data-ttu-id="ff5c7-149">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ff5c7-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ff5c7-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff5c7-150">NOTES</span></span>

## <span data-ttu-id="ff5c7-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff5c7-151">RELATED LINKS</span></span>

[<span data-ttu-id="ff5c7-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ff5c7-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
