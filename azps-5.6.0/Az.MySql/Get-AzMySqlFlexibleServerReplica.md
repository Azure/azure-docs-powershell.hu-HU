---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 25444df39945527d1bc574283e397407e0218633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924034"
---
# <span data-ttu-id="ffcd5-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="ffcd5-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="ffcd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcd5-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ffcd5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ffcd5-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ffcd5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ffcd5-105">DESCRIPTION</span></span>
<span data-ttu-id="ffcd5-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ffcd5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ffcd5-107">EXAMPLES</span></span>

### <span data-ttu-id="ffcd5-108">1. példa: A MySql-kiszolgálói replika lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="ffcd5-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="ffcd5-109">Ez a parancsmag a MySql-kiszolgálói replikát erőforráscsoport és kiszolgálónév alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="ffcd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffcd5-110">PARAMETERS</span></span>

### <span data-ttu-id="ffcd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcd5-111">-DefaultProfile</span></span>
<span data-ttu-id="ffcd5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcd5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcd5-113">-ResourceGroupName</span></span>
<span data-ttu-id="ffcd5-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-114">The name of the resource group.</span></span>
<span data-ttu-id="ffcd5-115">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ffcd5-115">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcd5-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffcd5-116">-ServerName</span></span>
<span data-ttu-id="ffcd5-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcd5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffcd5-118">-SubscriptionId</span></span>
<span data-ttu-id="ffcd5-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcd5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcd5-120">CommonParameters</span></span>
<span data-ttu-id="ffcd5-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffcd5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcd5-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffcd5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcd5-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffcd5-123">INPUTS</span></span>

## <span data-ttu-id="ffcd5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffcd5-124">OUTPUTS</span></span>

### <span data-ttu-id="ffcd5-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ffcd5-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="ffcd5-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ffcd5-126">NOTES</span></span>

<span data-ttu-id="ffcd5-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ffcd5-127">ALIASES</span></span>

## <span data-ttu-id="ffcd5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffcd5-128">RELATED LINKS</span></span>

