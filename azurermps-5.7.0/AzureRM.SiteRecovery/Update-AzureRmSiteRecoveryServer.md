---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: ce38334d3ae37864d53830970d895e29755f6687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492159"
---
# <span data-ttu-id="83e23-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83e23-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="83e23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83e23-102">SYNOPSIS</span></span>
<span data-ttu-id="83e23-103">Frissíti a webhely-helyreállítási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="83e23-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83e23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83e23-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83e23-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83e23-105">DESCRIPTION</span></span>
<span data-ttu-id="83e23-106">Az **Update-AzureRmSiteRecoveryServer** parancsmag frissíti az Azure webhely-helyreállítási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="83e23-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="83e23-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83e23-107">EXAMPLES</span></span>

## <span data-ttu-id="83e23-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83e23-108">PARAMETERS</span></span>

### <span data-ttu-id="83e23-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e23-109">-DefaultProfile</span></span>
<span data-ttu-id="83e23-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83e23-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e23-111">-Server</span><span class="sxs-lookup"><span data-stu-id="83e23-111">-Server</span></span>
<span data-ttu-id="83e23-112">A parancsmag által frissített webhely-helyreállítási kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="83e23-112">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e23-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e23-113">CommonParameters</span></span>
<span data-ttu-id="83e23-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83e23-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e23-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e23-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e23-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83e23-116">INPUTS</span></span>

### <span data-ttu-id="83e23-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="83e23-117">ASRServer</span></span>
<span data-ttu-id="83e23-118">A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="83e23-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="83e23-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83e23-119">OUTPUTS</span></span>

## <span data-ttu-id="83e23-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83e23-120">NOTES</span></span>

## <span data-ttu-id="83e23-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83e23-121">RELATED LINKS</span></span>

[<span data-ttu-id="83e23-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83e23-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="83e23-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="83e23-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
