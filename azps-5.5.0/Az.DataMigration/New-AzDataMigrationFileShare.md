---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165331"
---
# <span data-ttu-id="09fb8-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="09fb8-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="09fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="09fb8-103">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás FileShare objektumát, amely megadja a helyi hálózati megosztást, amelybe a forrásadatbázis biztonsági másolatát át kell vinni.</span><span class="sxs-lookup"><span data-stu-id="09fb8-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="09fb8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09fb8-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fb8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="09fb8-106">A New-AzDataMigrationFileShare parancsmag létrehozza a FileShare objektumot, amely megadja azt a helyi hálózati megosztást, amelybe az Azure Database Migration Service forrásadatbázis-biztonsági másolatot tud készíteni.</span><span class="sxs-lookup"><span data-stu-id="09fb8-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="09fb8-107">A forrás SQL Server-példányt futtató szolgáltatásfióknak írási jogosultsággal kell rendelkezik ehhez a hálózati megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="09fb8-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="09fb8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09fb8-108">EXAMPLES</span></span>

### <span data-ttu-id="09fb8-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="09fb8-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="09fb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="09fb8-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="09fb8-111">-Credential</span></span>
<span data-ttu-id="09fb8-112">Hitelesítő adatok a fájlmegosztás eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="09fb8-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fb8-113">-DefaultProfile</span></span>
<span data-ttu-id="09fb8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09fb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fb8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="09fb8-115">-Path</span></span>
<span data-ttu-id="09fb8-116">Fájlmegosztási útvonal.</span><span class="sxs-lookup"><span data-stu-id="09fb8-116">File share path.</span></span>

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

### <span data-ttu-id="09fb8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fb8-117">CommonParameters</span></span>
<span data-ttu-id="09fb8-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fb8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fb8-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fb8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fb8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09fb8-120">INPUTS</span></span>

### <span data-ttu-id="09fb8-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="09fb8-121">None</span></span>

## <span data-ttu-id="09fb8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fb8-122">OUTPUTS</span></span>

### <span data-ttu-id="09fb8-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="09fb8-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="09fb8-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09fb8-124">NOTES</span></span>

## <span data-ttu-id="09fb8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09fb8-125">RELATED LINKS</span></span>
