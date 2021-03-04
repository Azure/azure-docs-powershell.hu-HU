---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 7b47e54076441f1f4e78ec8cabc6a9dd3cd47153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919978"
---
# <span data-ttu-id="b1df0-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b1df0-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="b1df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1df0-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df0-103">Információkat kap a DataShare-fiókokról</span><span class="sxs-lookup"><span data-stu-id="b1df0-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="b1df0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1df0-104">SYNTAX</span></span>

### <span data-ttu-id="b1df0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1df0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1df0-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df0-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1df0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df0-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1df0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1df0-108">DESCRIPTION</span></span>
<span data-ttu-id="b1df0-109">A **Get-AzDataShareAccount** parancsmag információkat kap egy Azure-előfizetés vagy -erőforráscsoport adatmegosztási fiókjairól.</span><span class="sxs-lookup"><span data-stu-id="b1df0-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="b1df0-110">Ha megadja egy fiók nevét, ez a parancsmag információt kap a datshare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="b1df0-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="b1df0-111">Ha nem ad meg nevet, ez a parancsmag információt kap egy Azure-előfizetés/erőforráscsoport összes megosztott fiókáról.</span><span class="sxs-lookup"><span data-stu-id="b1df0-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="b1df0-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1df0-112">EXAMPLES</span></span>

### <span data-ttu-id="b1df0-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="b1df0-113">Example 1</span></span>
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

<span data-ttu-id="b1df0-114">Ez a parancs információkat jelenít meg az Azure-előfizetésben található összes adatmegosztási fiókról.</span><span class="sxs-lookup"><span data-stu-id="b1df0-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="b1df0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1df0-115">PARAMETERS</span></span>

### <span data-ttu-id="b1df0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df0-116">-DefaultProfile</span></span>
<span data-ttu-id="b1df0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1df0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1df0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b1df0-118">-Name</span></span>
<span data-ttu-id="b1df0-119">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="b1df0-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="b1df0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1df0-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1df0-121">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="b1df0-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="b1df0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1df0-122">-ResourceId</span></span>
<span data-ttu-id="b1df0-123">Az Azure-adat-megosztási fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1df0-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="b1df0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df0-124">CommonParameters</span></span>
<span data-ttu-id="b1df0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1df0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df0-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1df0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1df0-127">INPUTS</span></span>

### <span data-ttu-id="b1df0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1df0-128">System.String</span></span>

## <span data-ttu-id="b1df0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1df0-129">OUTPUTS</span></span>

### <span data-ttu-id="b1df0-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b1df0-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="b1df0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1df0-131">NOTES</span></span>

## <span data-ttu-id="b1df0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1df0-132">RELATED LINKS</span></span>
