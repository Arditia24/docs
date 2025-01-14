---
title: Configurar permisos para agregar colaboradores externos
intro: 'To protect your organization''s data and the number of paid licenses used in your organization, you can configure who can add outside collaborators to organization repositories.'
redirect_from:
  - /articles/restricting-the-ability-to-add-outside-collaborators-to-organization-repositories
  - /articles/setting-permissions-for-adding-outside-collaborators
  - /github/setting-up-and-managing-organizations-and-teams/setting-permissions-for-adding-outside-collaborators
versions:
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Configurar la política de colaboradores
---

Predeterminadamente, cualquiera con acceso administrativo en un repositorio puede invitar a los colaboradores externos a trabajar en el repositorio. You can choose to restrict the ability to add outside collaborators to organization owners only.

{% ifversion ghec %}
{% note %}

**Nota:** Solo las organizaciones que utilizan {% data variables.product.prodname_ghe_cloud %} pueden restringir la capacidad de invitar colaboradores externos para que solo sean los propietarios de organizaciones. {% data reusables.enterprise.link-to-ghec-trial %}

{% endnote %}
{% endif %}

{% ifversion ghec %}Si tu organización el pertenece a una cuenta empresarial, no podrás{% else %}No podrás{% endif %}configurar este ajuste para ella en caso de que un propietario de empresa haya configurado una política a nivel empresarial. Para obtener más información, consulta la sección "[Requerir políticas de administración de repositorios en tu empresa]{% ifversion ghec %}(/admin/policies/enforcing-policies-for-your-enterprise/enforcing-repository-management-policies-in-your-enterprise#enforcing-a-policy-for-inviting-collaborators-to-repositories)"{% else %}(/admin/policies/enforcing-policies-for-your-enterprise/enforcing-repository-management-policies-in-your-enterprise#enforcing-a-policy-for-inviting-outside-collaborators-to-repositories){% endif %}".

{% data reusables.organizations.outside-collaborators-use-seats %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.member-privileges %}{% ifversion ghes < 3.3 %}
5. En "Repository invitations" (Invitaciones al repositorio), selecciona **Allow members to invite outside collaborators to repositories for this organization** (Permitir que los miembros inviten colaboradores externos a los repositorios para esta organización). ![Checkbox to allow members to invite outside collaborators to organization repositories](/assets/images/help/organizations/repo-invitations-checkbox-old.png){% else %}
5. Under "Repository outside collaborators", deselect **Allow repository administrators to invite outside collaborators to repositories for this organization**. ![Checkbox to allow repository administrators to invite outside collaborators to organization repositories](/assets/images/help/organizations/repo-invitations-checkbox-updated.png){% endif %}
6. Haz clic en **Save ** (guardar).
