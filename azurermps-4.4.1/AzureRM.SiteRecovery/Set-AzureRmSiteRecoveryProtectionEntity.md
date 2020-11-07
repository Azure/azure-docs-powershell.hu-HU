---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679019"
---
# <span data-ttu-id="85fc8-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="85fc8-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="85fc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="85fc8-103">Beállítja a webhely-helyreállítási védelem entitás állapotát.</span><span class="sxs-lookup"><span data-stu-id="85fc8-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85fc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85fc8-104">SYNTAX</span></span>

### <span data-ttu-id="85fc8-105">Letiltó (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85fc8-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85fc8-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="85fc8-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85fc8-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="85fc8-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85fc8-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="85fc8-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85fc8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="85fc8-109">DESCRIPTION</span></span>
<span data-ttu-id="85fc8-110">A **set-AzureRmSiteRecoveryProtectionEntity** parancsmag engedélyezi vagy letiltja a védelmet az Azure webhely-helyreállítási védelmi entitások számára.</span><span class="sxs-lookup"><span data-stu-id="85fc8-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="85fc8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="85fc8-111">EXAMPLES</span></span>

## <span data-ttu-id="85fc8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85fc8-112">PARAMETERS</span></span>

### <span data-ttu-id="85fc8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="85fc8-113">-Force</span></span>
<span data-ttu-id="85fc8-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="85fc8-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-115">-OS</span><span class="sxs-lookup"><span data-stu-id="85fc8-115">-OS</span></span>
<span data-ttu-id="85fc8-116">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85fc8-116">Specifies the operating system type.</span></span>
<span data-ttu-id="85fc8-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="85fc8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85fc8-118">Windows</span><span class="sxs-lookup"><span data-stu-id="85fc8-118">Windows</span></span>
- <span data-ttu-id="85fc8-119">Linux</span><span class="sxs-lookup"><span data-stu-id="85fc8-119">Linux</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="85fc8-120">-OSDiskName</span></span>
<span data-ttu-id="85fc8-121">Az operációs rendszert tartalmazó lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85fc8-121">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="85fc8-122">-Policy</span></span>
<span data-ttu-id="85fc8-123">A webhely-helyreállítási házirend objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85fc8-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-124">-Védelem</span><span class="sxs-lookup"><span data-stu-id="85fc8-124">-Protection</span></span>
<span data-ttu-id="85fc8-125">Megadja, hogy engedélyezve vagy le kell-e tiltani a védelmet.</span><span class="sxs-lookup"><span data-stu-id="85fc8-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="85fc8-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="85fc8-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85fc8-127">Engedélyezése</span><span class="sxs-lookup"><span data-stu-id="85fc8-127">Enable</span></span>
- <span data-ttu-id="85fc8-128">Megbénít</span><span class="sxs-lookup"><span data-stu-id="85fc8-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="85fc8-129">-ProtectionEntity</span></span>
<span data-ttu-id="85fc8-130">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85fc8-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="85fc8-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="85fc8-132">A cél Azure-tároló fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85fc8-132">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="85fc8-133">-WaitForCompletion</span></span>
<span data-ttu-id="85fc8-134">Jelzi, hogy a parancs a visszatérés előtt várja a befejezést.</span><span class="sxs-lookup"><span data-stu-id="85fc8-134">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85fc8-135">-Confirm</span></span>
<span data-ttu-id="85fc8-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85fc8-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85fc8-137">-WhatIf</span></span>
<span data-ttu-id="85fc8-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85fc8-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="85fc8-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85fc8-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85fc8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85fc8-140">-DefaultProfile</span></span>
<span data-ttu-id="85fc8-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85fc8-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85fc8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85fc8-142">CommonParameters</span></span>
<span data-ttu-id="85fc8-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85fc8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85fc8-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85fc8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85fc8-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85fc8-145">INPUTS</span></span>

### <span data-ttu-id="85fc8-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="85fc8-146">ASRProtectionEntity</span></span>
<span data-ttu-id="85fc8-147">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="85fc8-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="85fc8-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85fc8-148">OUTPUTS</span></span>

### <span data-ttu-id="85fc8-149">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="85fc8-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="85fc8-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85fc8-150">NOTES</span></span>

## <span data-ttu-id="85fc8-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85fc8-151">RELATED LINKS</span></span>

[<span data-ttu-id="85fc8-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="85fc8-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
