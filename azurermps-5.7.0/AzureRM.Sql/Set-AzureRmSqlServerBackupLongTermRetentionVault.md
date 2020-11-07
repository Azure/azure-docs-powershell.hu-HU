---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0abdfdb78c8564afd4cac2661c4f390f5831b73f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679651"
---
# <span data-ttu-id="b362f-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b362f-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="b362f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b362f-102">SYNOPSIS</span></span>
<span data-ttu-id="b362f-103">Hosszú távú adatmegőrzési boltozatot állít be.</span><span class="sxs-lookup"><span data-stu-id="b362f-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b362f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b362f-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b362f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b362f-105">DESCRIPTION</span></span>
<span data-ttu-id="b362f-106">A **set-AzureRmSqlServerBackupLongTermRetentionVault** parancsmag a kiszolgálón regisztrált hosszú távú adatmegőrzési boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="b362f-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="b362f-107">A boltozat a biztonsági másolatok adatainak tárolására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b362f-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="b362f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b362f-108">EXAMPLES</span></span>

## <span data-ttu-id="b362f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b362f-109">PARAMETERS</span></span>

### <span data-ttu-id="b362f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b362f-110">-DefaultProfile</span></span>
<span data-ttu-id="b362f-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b362f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b362f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b362f-112">-ResourceGroupName</span></span>
<span data-ttu-id="b362f-113">A kiszolgálót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b362f-113">Specifies the name of the resource group that contains the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b362f-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b362f-114">-ResourceId</span></span>
<span data-ttu-id="b362f-115">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b362f-115">Specifies the ID of a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b362f-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b362f-116">-ServerName</span></span>
<span data-ttu-id="b362f-117">Azt a kiszolgálót adja meg, amelynek a parancsmagja a boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="b362f-117">Specifies the server for which this cmdlet sets a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b362f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b362f-118">-Confirm</span></span>
<span data-ttu-id="b362f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b362f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b362f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b362f-120">-WhatIf</span></span>
<span data-ttu-id="b362f-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b362f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b362f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b362f-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b362f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b362f-123">CommonParameters</span></span>
<span data-ttu-id="b362f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b362f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b362f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b362f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b362f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b362f-126">INPUTS</span></span>

### <span data-ttu-id="b362f-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="b362f-127">None</span></span>
<span data-ttu-id="b362f-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b362f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b362f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b362f-129">OUTPUTS</span></span>

## <span data-ttu-id="b362f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b362f-130">NOTES</span></span>

## <span data-ttu-id="b362f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b362f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b362f-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b362f-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="b362f-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b362f-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
