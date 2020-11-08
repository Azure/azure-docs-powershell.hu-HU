---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: e70de343c064eadd846b2df150ef6a808b1bf044
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010963"
---
# <span data-ttu-id="da9e2-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="da9e2-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="da9e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="da9e2-103">Információt kap az DataShare-fiókokról</span><span class="sxs-lookup"><span data-stu-id="da9e2-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="da9e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da9e2-104">SYNTAX</span></span>

### <span data-ttu-id="da9e2-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da9e2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9e2-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9e2-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da9e2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9e2-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9e2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="da9e2-108">DESCRIPTION</span></span>
<span data-ttu-id="da9e2-109">A **Get-AzDataShareAccount** parancsmag az Azure-előfizetés/erőforráscsoport DataShare-fiókjairól szóló információkat kap.</span><span class="sxs-lookup"><span data-stu-id="da9e2-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="da9e2-110">Ha megad egy fiók nevét, ez a parancsmag információkat kap az datshare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="da9e2-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="da9e2-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az Azure-előfizetés/erőforráscsoport összes DataShare-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="da9e2-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="da9e2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="da9e2-112">EXAMPLES</span></span>

### <span data-ttu-id="da9e2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da9e2-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="da9e2-114">Ez a parancs információt jelenít meg az Azure-előfizetéshez tartozó összes DataShare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="da9e2-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="da9e2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da9e2-115">PARAMETERS</span></span>

### <span data-ttu-id="da9e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9e2-116">-DefaultProfile</span></span>
<span data-ttu-id="da9e2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da9e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da9e2-118">-Name</span></span>
<span data-ttu-id="da9e2-119">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="da9e2-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="da9e2-121">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="da9e2-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9e2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da9e2-122">-ResourceId</span></span>
<span data-ttu-id="da9e2-123">Az Azure Data Share-fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da9e2-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da9e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9e2-124">CommonParameters</span></span>
<span data-ttu-id="da9e2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da9e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9e2-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9e2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9e2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9e2-127">INPUTS</span></span>

### <span data-ttu-id="da9e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="da9e2-128">System.String</span></span>

## <span data-ttu-id="da9e2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9e2-129">OUTPUTS</span></span>

### <span data-ttu-id="da9e2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="da9e2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="da9e2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da9e2-131">NOTES</span></span>

## <span data-ttu-id="da9e2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da9e2-132">RELATED LINKS</span></span>
