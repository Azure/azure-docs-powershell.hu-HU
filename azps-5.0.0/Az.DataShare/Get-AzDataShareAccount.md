---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297548"
---
# <span data-ttu-id="4ae6e-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="4ae6e-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="4ae6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ae6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae6e-103">Információt kap az DataShare-fiókokról</span><span class="sxs-lookup"><span data-stu-id="4ae6e-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="4ae6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ae6e-104">SYNTAX</span></span>

### <span data-ttu-id="4ae6e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ae6e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae6e-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ae6e-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ae6e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ae6e-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae6e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ae6e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae6e-109">A **Get-AzDataShareAccount** parancsmag az Azure-előfizetés/erőforráscsoport DataShare-fiókjairól szóló információkat kap.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="4ae6e-110">Ha megad egy fiók nevét, ez a parancsmag információkat kap az datshare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="4ae6e-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az Azure-előfizetés/erőforráscsoport összes DataShare-fiókjáról.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="4ae6e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4ae6e-112">EXAMPLES</span></span>

### <span data-ttu-id="4ae6e-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ae6e-113">Example 1</span></span>
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

<span data-ttu-id="4ae6e-114">Ez a parancs információt jelenít meg az Azure-előfizetéshez tartozó összes DataShare-fiókról.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="4ae6e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ae6e-115">PARAMETERS</span></span>

### <span data-ttu-id="4ae6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae6e-116">-DefaultProfile</span></span>
<span data-ttu-id="4ae6e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae6e-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ae6e-118">-Name</span></span>
<span data-ttu-id="4ae6e-119">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="4ae6e-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="4ae6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ae6e-121">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="4ae6e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae6e-122">-ResourceId</span></span>
<span data-ttu-id="4ae6e-123">Az Azure Data Share-fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="4ae6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae6e-124">CommonParameters</span></span>
<span data-ttu-id="4ae6e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ae6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae6e-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae6e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ae6e-127">INPUTS</span></span>

### <span data-ttu-id="4ae6e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae6e-128">System.String</span></span>

## <span data-ttu-id="4ae6e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ae6e-129">OUTPUTS</span></span>

### <span data-ttu-id="4ae6e-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="4ae6e-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="4ae6e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ae6e-131">NOTES</span></span>

## <span data-ttu-id="4ae6e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ae6e-132">RELATED LINKS</span></span>
