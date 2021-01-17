---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326475"
---
# <span data-ttu-id="121d2-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="121d2-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="121d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121d2-102">SYNOPSIS</span></span>
<span data-ttu-id="121d2-103">Információkat kap a DataShare-fiókokról</span><span class="sxs-lookup"><span data-stu-id="121d2-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="121d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="121d2-104">SYNTAX</span></span>

### <span data-ttu-id="121d2-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="121d2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="121d2-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="121d2-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="121d2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="121d2-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121d2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="121d2-108">DESCRIPTION</span></span>
<span data-ttu-id="121d2-109">A **Get-AzDataShareAccount** parancsmag információkat kap egy Azure-előfizetés vagy -erőforráscsoport adatmegosztási fiókjairól.</span><span class="sxs-lookup"><span data-stu-id="121d2-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="121d2-110">Ha megadja egy fiók nevét, ez a parancsmag információt kap a datshare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="121d2-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="121d2-111">Ha nem ad meg nevet, ez a parancsmag információt kap egy Azure-előfizetés/erőforráscsoport összes megosztott fiókáról.</span><span class="sxs-lookup"><span data-stu-id="121d2-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="121d2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="121d2-112">EXAMPLES</span></span>

### <span data-ttu-id="121d2-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="121d2-113">Example 1</span></span>
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

<span data-ttu-id="121d2-114">Ez a parancs információkat jelenít meg az Azure-előfizetésben található összes adatmegosztási fiókról.</span><span class="sxs-lookup"><span data-stu-id="121d2-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="121d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121d2-115">PARAMETERS</span></span>

### <span data-ttu-id="121d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121d2-116">-DefaultProfile</span></span>
<span data-ttu-id="121d2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="121d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121d2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="121d2-118">-Name</span></span>
<span data-ttu-id="121d2-119">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="121d2-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="121d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="121d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="121d2-121">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="121d2-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="121d2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="121d2-122">-ResourceId</span></span>
<span data-ttu-id="121d2-123">Az Azure-adat-megosztási fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="121d2-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="121d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121d2-124">CommonParameters</span></span>
<span data-ttu-id="121d2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121d2-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="121d2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121d2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="121d2-127">INPUTS</span></span>

### <span data-ttu-id="121d2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="121d2-128">System.String</span></span>

## <span data-ttu-id="121d2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="121d2-129">OUTPUTS</span></span>

### <span data-ttu-id="121d2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="121d2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="121d2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="121d2-131">NOTES</span></span>

## <span data-ttu-id="121d2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="121d2-132">RELATED LINKS</span></span>
