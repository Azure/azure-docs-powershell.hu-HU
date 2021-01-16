---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358930"
---
# <span data-ttu-id="0c3db-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="0c3db-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="0c3db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3db-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3db-103">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="0c3db-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0c3db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c3db-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0c3db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c3db-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3db-106">List all the replicas for a given server.</span><span class="sxs-lookup"><span data-stu-id="0c3db-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0c3db-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c3db-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3db-108">1. példa: A MySql-kiszolgálói replika lekérte erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="0c3db-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0c3db-109">Ez a parancsmag a MySql-kiszolgálói replikát erőforráscsoport és kiszolgálónév alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3db-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="0c3db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c3db-110">PARAMETERS</span></span>

### <span data-ttu-id="0c3db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3db-111">-DefaultProfile</span></span>
<span data-ttu-id="0c3db-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c3db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3db-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3db-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c3db-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0c3db-114">The name of the resource group.</span></span>
<span data-ttu-id="0c3db-115">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0c3db-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0c3db-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0c3db-116">-ServerName</span></span>
<span data-ttu-id="0c3db-117">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0c3db-117">The name of the server.</span></span>

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

### <span data-ttu-id="0c3db-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c3db-118">-SubscriptionId</span></span>
<span data-ttu-id="0c3db-119">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c3db-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0c3db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3db-120">CommonParameters</span></span>
<span data-ttu-id="0c3db-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3db-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c3db-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3db-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c3db-123">INPUTS</span></span>

## <span data-ttu-id="0c3db-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3db-124">OUTPUTS</span></span>

### <span data-ttu-id="0c3db-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="0c3db-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0c3db-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c3db-126">NOTES</span></span>

<span data-ttu-id="0c3db-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0c3db-127">ALIASES</span></span>

## <span data-ttu-id="0c3db-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c3db-128">RELATED LINKS</span></span>

