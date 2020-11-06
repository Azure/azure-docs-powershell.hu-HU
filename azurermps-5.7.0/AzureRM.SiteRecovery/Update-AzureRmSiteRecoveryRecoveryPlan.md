---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492160"
---
# <span data-ttu-id="21c13-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="21c13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21c13-102">SYNOPSIS</span></span>
<span data-ttu-id="21c13-103">Helyreállítási terv frissítése a webhely-helyreállításban.</span><span class="sxs-lookup"><span data-stu-id="21c13-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21c13-104">SYNTAX</span></span>

### <span data-ttu-id="21c13-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21c13-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c13-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="21c13-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21c13-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="21c13-107">DESCRIPTION</span></span>
<span data-ttu-id="21c13-108">Az **Update-AzureRmSiteRecoveryRecoveryPlan** parancsmag az Azure-webhely helyreállításakor frissíti a helyreállítási tervet, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="21c13-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="21c13-109">Példák</span><span class="sxs-lookup"><span data-stu-id="21c13-109">EXAMPLES</span></span>

### <span data-ttu-id="21c13-110">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="21c13-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="21c13-111">Ez a parancs frissíti a megadott helyreállítási csomagot, majd közzéteszi azt.</span><span class="sxs-lookup"><span data-stu-id="21c13-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="21c13-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21c13-112">PARAMETERS</span></span>

### <span data-ttu-id="21c13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c13-113">-DefaultProfile</span></span>
<span data-ttu-id="21c13-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21c13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c13-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="21c13-115">-Path</span></span>
<span data-ttu-id="21c13-116">A parancsmag által frissített helyreállítási terv helyreállítási tervének elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="21c13-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-117">-RecoveryPlan</span></span>
<span data-ttu-id="21c13-118">Meghatározza, hogy a parancsmag milyen helyreállítási csomagot frissít.</span><span class="sxs-lookup"><span data-stu-id="21c13-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c13-119">CommonParameters</span></span>
<span data-ttu-id="21c13-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21c13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c13-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c13-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c13-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c13-122">INPUTS</span></span>

### <span data-ttu-id="21c13-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="21c13-124">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="21c13-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="21c13-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c13-125">OUTPUTS</span></span>

## <span data-ttu-id="21c13-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21c13-126">NOTES</span></span>

## <span data-ttu-id="21c13-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21c13-127">RELATED LINKS</span></span>

[<span data-ttu-id="21c13-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="21c13-129">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="21c13-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21c13-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


