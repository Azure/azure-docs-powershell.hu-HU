---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680477"
---
# <span data-ttu-id="f8a94-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f8a94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8a94-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a94-103">Helyreállítási terv frissítése a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="f8a94-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8a94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8a94-104">SYNTAX</span></span>

### <span data-ttu-id="f8a94-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8a94-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a94-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="f8a94-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8a94-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8a94-107">DESCRIPTION</span></span>
<span data-ttu-id="f8a94-108">Az **Update-AzureRmSiteRecoveryRecoveryPlan** parancsmag az Azure-webhely helyreállításakor frissíti a helyreállítási tervet, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="f8a94-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="f8a94-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f8a94-109">EXAMPLES</span></span>

### <span data-ttu-id="f8a94-110">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="f8a94-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="f8a94-111">Ez a parancs frissíti a megadott helyreállítási csomagot, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="f8a94-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="f8a94-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8a94-112">PARAMETERS</span></span>

### <span data-ttu-id="f8a94-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f8a94-113">-Path</span></span>
<span data-ttu-id="f8a94-114">A parancsmag által frissített helyreállítási terv helyreállítási tervének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8a94-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a94-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-115">-RecoveryPlan</span></span>
<span data-ttu-id="f8a94-116">Meghatározza, hogy a parancsmag milyen helyreállítási csomagot frissít.</span><span class="sxs-lookup"><span data-stu-id="f8a94-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a94-117">-DefaultProfile</span></span>
<span data-ttu-id="f8a94-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8a94-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8a94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a94-119">CommonParameters</span></span>
<span data-ttu-id="f8a94-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8a94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a94-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a94-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a94-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8a94-122">INPUTS</span></span>

### <span data-ttu-id="f8a94-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="f8a94-124">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f8a94-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="f8a94-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8a94-125">OUTPUTS</span></span>

## <span data-ttu-id="f8a94-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8a94-126">NOTES</span></span>

## <span data-ttu-id="f8a94-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8a94-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8a94-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f8a94-129">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f8a94-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8a94-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


