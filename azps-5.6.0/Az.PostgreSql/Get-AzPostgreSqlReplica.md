---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: c8fea3c7d0cfca227a69f83a76d73617d69106a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919481"
---
# <span data-ttu-id="082a8-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="082a8-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="082a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="082a8-102">SYNOPSIS</span></span>
<span data-ttu-id="082a8-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="082a8-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="082a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="082a8-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="082a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="082a8-105">DESCRIPTION</span></span>
<span data-ttu-id="082a8-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="082a8-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="082a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="082a8-107">EXAMPLES</span></span>

### <span data-ttu-id="082a8-108">1. példa: A PostgreSql-kiszolgálói replika lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="082a8-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="082a8-109">Ez a parancsmag erőforráscsoport és kiszolgálónév szerint kapja meg a PostgreSql-kiszolgálói replikát.</span><span class="sxs-lookup"><span data-stu-id="082a8-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="082a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="082a8-110">PARAMETERS</span></span>

### <span data-ttu-id="082a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082a8-111">-DefaultProfile</span></span>
<span data-ttu-id="082a8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="082a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082a8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082a8-113">-ResourceGroupName</span></span>
<span data-ttu-id="082a8-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="082a8-114">The name of the resource group.</span></span>
<span data-ttu-id="082a8-115">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="082a8-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="082a8-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="082a8-116">-ServerName</span></span>
<span data-ttu-id="082a8-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="082a8-117">The name of the server.</span></span>

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

### <span data-ttu-id="082a8-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="082a8-118">-SubscriptionId</span></span>
<span data-ttu-id="082a8-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="082a8-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="082a8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082a8-120">CommonParameters</span></span>
<span data-ttu-id="082a8-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082a8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082a8-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="082a8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082a8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="082a8-123">INPUTS</span></span>

## <span data-ttu-id="082a8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="082a8-124">OUTPUTS</span></span>

### <span data-ttu-id="082a8-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="082a8-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="082a8-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="082a8-126">NOTES</span></span>

<span data-ttu-id="082a8-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="082a8-127">ALIASES</span></span>

## <span data-ttu-id="082a8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="082a8-128">RELATED LINKS</span></span>

