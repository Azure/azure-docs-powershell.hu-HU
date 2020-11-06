---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502395"
---
# <span data-ttu-id="9ed4e-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="9ed4e-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="9ed4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ed4e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed4e-103">Beolvashatja a tárterület besorolását a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="9ed4e-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ed4e-104">SYNTAX</span></span>

### <span data-ttu-id="9ed4e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ed4e-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed4e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9ed4e-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ed4e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9ed4e-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ed4e-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="9ed4e-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ed4e-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="9ed4e-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ed4e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ed4e-110">DESCRIPTION</span></span>
<span data-ttu-id="9ed4e-111">A **Get-AzureRmSiteRecoveryStorageClassification** parancsmag a tárolási besorolásokat az Azure webhely-helyreállításban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ed4e-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="9ed4e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9ed4e-112">EXAMPLES</span></span>

## <span data-ttu-id="9ed4e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ed4e-113">PARAMETERS</span></span>

### <span data-ttu-id="9ed4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed4e-114">-DefaultProfile</span></span>
<span data-ttu-id="9ed4e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ed4e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed4e-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="9ed4e-116">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed4e-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="9ed4e-117">-FriendlyName</span></span>
<span data-ttu-id="9ed4e-118">Annak a tárolási osztályozásnak a rövid nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="9ed4e-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed4e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ed4e-119">-Name</span></span>
<span data-ttu-id="9ed4e-120">Annak a tárolási osztályozásnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="9ed4e-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed4e-121">-Server</span><span class="sxs-lookup"><span data-stu-id="9ed4e-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed4e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed4e-122">CommonParameters</span></span>
<span data-ttu-id="9ed4e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ed4e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed4e-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed4e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed4e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed4e-125">INPUTS</span></span>

### <span data-ttu-id="9ed4e-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9ed4e-126">ASRFabric</span></span>
<span data-ttu-id="9ed4e-127">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9ed4e-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="9ed4e-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="9ed4e-128">ASRServer</span></span>
<span data-ttu-id="9ed4e-129">A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9ed4e-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="9ed4e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed4e-130">OUTPUTS</span></span>

### <span data-ttu-id="9ed4e-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="9ed4e-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="9ed4e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ed4e-132">NOTES</span></span>

## <span data-ttu-id="9ed4e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ed4e-133">RELATED LINKS</span></span>

