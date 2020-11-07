---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672511"
---
# <span data-ttu-id="8acb7-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="8acb7-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="8acb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8acb7-102">SYNOPSIS</span></span>
<span data-ttu-id="8acb7-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="8acb7-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8acb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8acb7-104">SYNTAX</span></span>

### <span data-ttu-id="8acb7-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8acb7-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8acb7-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="8acb7-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8acb7-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="8acb7-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8acb7-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="8acb7-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8acb7-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="8acb7-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8acb7-110">ByName</span><span class="sxs-lookup"><span data-stu-id="8acb7-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8acb7-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8acb7-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acb7-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="8acb7-112">DESCRIPTION</span></span>
<span data-ttu-id="8acb7-113">A **Get-AzureRmSiteRecoveryNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="8acb7-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8acb7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="8acb7-114">EXAMPLES</span></span>

## <span data-ttu-id="8acb7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8acb7-115">PARAMETERS</span></span>

### <span data-ttu-id="8acb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acb7-116">-DefaultProfile</span></span>
<span data-ttu-id="8acb7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8acb7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acb7-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="8acb7-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acb7-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="8acb7-119">-FriendlyName</span></span>
<span data-ttu-id="8acb7-120">A virtuálisgép-hálózat rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8acb7-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acb7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8acb7-121">-Name</span></span>
<span data-ttu-id="8acb7-122">A virtuális gép hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8acb7-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acb7-123">-Server</span><span class="sxs-lookup"><span data-stu-id="8acb7-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acb7-124">CommonParameters</span></span>
<span data-ttu-id="8acb7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8acb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acb7-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8acb7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acb7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8acb7-127">INPUTS</span></span>

### <span data-ttu-id="8acb7-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8acb7-128">ASRFabric</span></span>
<span data-ttu-id="8acb7-129">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="8acb7-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8acb7-130">String</span></span>
<span data-ttu-id="8acb7-131">A ' típusú megjelenített ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8acb7-132">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8acb7-132">String</span></span>
<span data-ttu-id="8acb7-133">A ' típusú megjelenített ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8acb7-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8acb7-134">String</span></span>
<span data-ttu-id="8acb7-135">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8acb7-136">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8acb7-136">String</span></span>
<span data-ttu-id="8acb7-137">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8acb7-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="8acb7-138">ASRServer</span></span>
<span data-ttu-id="8acb7-139">A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8acb7-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="8acb7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8acb7-140">OUTPUTS</span></span>

### <span data-ttu-id="8acb7-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="8acb7-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="8acb7-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8acb7-142">NOTES</span></span>

## <span data-ttu-id="8acb7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8acb7-143">RELATED LINKS</span></span>

