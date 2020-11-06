---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504263"
---
# <span data-ttu-id="ed12e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="ed12e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="ed12e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed12e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed12e-103">Hosszú távú adatmegőrzési boltozatot állít be.</span><span class="sxs-lookup"><span data-stu-id="ed12e-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed12e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed12e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed12e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed12e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed12e-106">A **set-AzureRmSqlServerBackupLongTermRetentionVault** parancsmag a kiszolgálón regisztrált hosszú távú adatmegőrzési boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="ed12e-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="ed12e-107">A boltozat a biztonsági másolatok adatainak tárolására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ed12e-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="ed12e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ed12e-108">EXAMPLES</span></span>

## <span data-ttu-id="ed12e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed12e-109">PARAMETERS</span></span>

### <span data-ttu-id="ed12e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed12e-110">-DefaultProfile</span></span>
<span data-ttu-id="ed12e-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ed12e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed12e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed12e-112">-ResourceGroupName</span></span>
<span data-ttu-id="ed12e-113">A kiszolgálót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed12e-113">Specifies the name of the resource group that contains the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed12e-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed12e-114">-ResourceId</span></span>
<span data-ttu-id="ed12e-115">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed12e-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed12e-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ed12e-116">-ServerName</span></span>
<span data-ttu-id="ed12e-117">Azt a kiszolgálót adja meg, amelynek a parancsmagja a boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="ed12e-117">Specifies the server for which this cmdlet sets a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed12e-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed12e-118">-Confirm</span></span>
<span data-ttu-id="ed12e-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed12e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed12e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed12e-120">-WhatIf</span></span>
<span data-ttu-id="ed12e-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed12e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed12e-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed12e-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed12e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed12e-123">CommonParameters</span></span>
<span data-ttu-id="ed12e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed12e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed12e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed12e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed12e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed12e-126">INPUTS</span></span>

### <span data-ttu-id="ed12e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ed12e-127">System.String</span></span>

## <span data-ttu-id="ed12e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed12e-128">OUTPUTS</span></span>

### <span data-ttu-id="ed12e-129">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="ed12e-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="ed12e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed12e-130">NOTES</span></span>

## <span data-ttu-id="ed12e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed12e-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed12e-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="ed12e-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="ed12e-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ed12e-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)