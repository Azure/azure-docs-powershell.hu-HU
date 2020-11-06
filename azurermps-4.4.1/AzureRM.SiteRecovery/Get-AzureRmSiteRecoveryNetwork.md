---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494654"
---
# <span data-ttu-id="2f8f0-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="2f8f0-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="2f8f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8f0-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="2f8f0-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f8f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f8f0-104">SYNTAX</span></span>

### <span data-ttu-id="2f8f0-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f8f0-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="2f8f0-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="2f8f0-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="2f8f0-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="2f8f0-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-110">ByName</span><span class="sxs-lookup"><span data-stu-id="2f8f0-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8f0-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f8f0-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f8f0-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f8f0-112">DESCRIPTION</span></span>
<span data-ttu-id="2f8f0-113">A **Get-AzureRmSiteRecoveryNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="2f8f0-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2f8f0-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2f8f0-114">EXAMPLES</span></span>

## <span data-ttu-id="2f8f0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f8f0-115">PARAMETERS</span></span>

### <span data-ttu-id="2f8f0-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="2f8f0-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f0-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="2f8f0-117">-FriendlyName</span></span>
<span data-ttu-id="2f8f0-118">A virtuálisgép-hálózat rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f8f0-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f8f0-119">-Name</span></span>
<span data-ttu-id="2f8f0-120">A virtuális gép hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f8f0-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f0-121">-Server</span><span class="sxs-lookup"><span data-stu-id="2f8f0-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8f0-122">-DefaultProfile</span></span>
<span data-ttu-id="2f8f0-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f8f0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f8f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8f0-124">CommonParameters</span></span>
<span data-ttu-id="2f8f0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f8f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8f0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f8f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8f0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f8f0-127">INPUTS</span></span>

### <span data-ttu-id="2f8f0-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2f8f0-128">ASRFabric</span></span>
<span data-ttu-id="2f8f0-129">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="2f8f0-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="2f8f0-130">String</span></span>
<span data-ttu-id="2f8f0-131">A ' típusú megjelenített ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2f8f0-132">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="2f8f0-132">String</span></span>
<span data-ttu-id="2f8f0-133">A ' típusú megjelenített ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2f8f0-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="2f8f0-134">String</span></span>
<span data-ttu-id="2f8f0-135">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2f8f0-136">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="2f8f0-136">String</span></span>
<span data-ttu-id="2f8f0-137">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2f8f0-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="2f8f0-138">ASRServer</span></span>
<span data-ttu-id="2f8f0-139">A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f8f0-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="2f8f0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f8f0-140">OUTPUTS</span></span>

### <span data-ttu-id="2f8f0-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="2f8f0-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="2f8f0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f8f0-142">NOTES</span></span>

## <span data-ttu-id="2f8f0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f8f0-143">RELATED LINKS</span></span>

