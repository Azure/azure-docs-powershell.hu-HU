---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 663ac3d8342e5ba231276e560408f8f7f6e74741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680748"
---
# <span data-ttu-id="1734e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="1734e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="1734e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1734e-102">SYNOPSIS</span></span>
<span data-ttu-id="1734e-103">Hosszú távú adatmegőrzési boltozatot állít be.</span><span class="sxs-lookup"><span data-stu-id="1734e-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1734e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1734e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1734e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1734e-105">DESCRIPTION</span></span>
<span data-ttu-id="1734e-106">A **set-AzureRmSqlServerBackupLongTermRetentionVault** parancsmag a kiszolgálón regisztrált hosszú távú adatmegőrzési boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="1734e-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="1734e-107">A boltozat a biztonsági másolatok adatainak tárolására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1734e-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="1734e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1734e-108">EXAMPLES</span></span>

## <span data-ttu-id="1734e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1734e-109">PARAMETERS</span></span>

### <span data-ttu-id="1734e-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1734e-110">-ResourceGroupName</span></span>
<span data-ttu-id="1734e-111">A kiszolgálót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1734e-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="1734e-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1734e-112">-ResourceId</span></span>
<span data-ttu-id="1734e-113">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1734e-113">Specifies the ID of a resource.</span></span>

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

### <span data-ttu-id="1734e-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1734e-114">-ServerName</span></span>
<span data-ttu-id="1734e-115">Azt a kiszolgálót adja meg, amelynek a parancsmagja a boltozatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="1734e-115">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="1734e-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1734e-116">-Confirm</span></span>
<span data-ttu-id="1734e-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1734e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1734e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1734e-118">-WhatIf</span></span>
<span data-ttu-id="1734e-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1734e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1734e-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1734e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1734e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1734e-121">-DefaultProfile</span></span>
<span data-ttu-id="1734e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1734e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1734e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1734e-123">CommonParameters</span></span>
<span data-ttu-id="1734e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1734e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1734e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1734e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1734e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1734e-126">INPUTS</span></span>

## <span data-ttu-id="1734e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1734e-127">OUTPUTS</span></span>

## <span data-ttu-id="1734e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1734e-128">NOTES</span></span>

## <span data-ttu-id="1734e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1734e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1734e-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="1734e-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="1734e-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1734e-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
